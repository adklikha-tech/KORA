---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Event Triggers guide

![Likha Control Room - Robots](../../images/control-room-robots.png)

Event triggers let you define when a saved flow should start from the Control Room Robots page.

Use event triggers when a flow should run because something happened outside the designer, such as an HTTP request arriving, a file appearing, a queue receiving work, or a Windows event being written.

## Where event triggers are managed

Open Control Room, then go to:

```txt
Robots > Event triggers
```

Click:

```txt
+ Add trigger
```

Then choose:

```txt
Trigger name
Flow
Trigger type
Parameters
Enabled
```

Click `Save trigger` to store the trigger definition.

## Current MVP behavior

Event trigger definitions are stored in Control Room with the selected flow and parameter values.

The Robot Service can use these definitions to watch for events and enqueue flows. Some trigger types may require the Robot Service or a future listener implementation to actively monitor the source event.

Schedules created in the Scheduler page are already handled by the scheduler. `Scheduled` event triggers use the same parameter shape so they can be routed through the Robots trigger system.

## Common fields

Every trigger has these fields:

```txt
Trigger name   Friendly name shown in Control Room
Flow           Flow to run when the trigger fires
Trigger type   Event source
Enabled        Whether the trigger can be used
```

The parameters shown below are saved as the trigger `config`.

## When Http request is received

Use this trigger when an external system should start a flow by calling a generated HTTP URL.

Parameters:

```txt
Http URL                  Generated URL for the caller
Request Body JSON Schema  Expected JSON body shape
Method                    Optional HTTP method filter
Relative path             Optional custom path for the endpoint
```

Example request body schema:

```json
{
  "type": "object",
  "properties": {
    "customer_id": {
      "type": "string"
    },
    "amount": {
      "type": "number"
    }
  },
  "required": ["customer_id"]
}
```

Typical use:

1. Add the trigger.
2. Copy the generated `Http URL`.
3. Give the URL to the calling application.
4. Set `Method` to `POST` if the caller posts JSON.
5. Save the expected request body schema.

## Scheduled

Use this trigger when a flow should run at a time or interval.

Parameters match the Scheduler page:

```txt
Run once                 Run at one date and time
Every hour / every N     Start at a date and time, then repeat every N hours
Every week               Run on a selected day and time
Cron expression          Advanced schedule using minute hour day month weekday
Notes                    Optional description
```

Cron example:

```txt
0 9 * * 1
```

This means every Monday at 09:00.

## Email received

Use this trigger when a mailbox message should start a flow.

Parameters:

```txt
Email address              Mailbox to monitor
Folder                     Mail folder, usually Inbox
Subject contains           Optional subject text filter
From address               Optional sender filter
Only when attachments exist Optional attachment filter
```

Typical use:

1. Enter the mailbox address.
2. Keep `Folder` as `Inbox` unless the mailbox uses another folder.
3. Add a subject or sender filter to avoid starting the flow for every email.
4. Enable `Only when attachments exist` for invoice, report, or document intake flows.

## File

Use this trigger when a specific file should start a flow after it is created, changed, or deleted.

Parameters:

```txt
File path          Full path to the file
Change type        Created, Modified, Deleted, or Created or Modified
File name filter   Optional wildcard filter
Debounce seconds   Wait time before firing after a change
```

Example:

```txt
File path: C:\Input\orders.xlsx
Change type: Created or Modified
File name filter: *.xlsx
Debounce seconds: 2
```

Use debounce seconds when another application writes the file in multiple steps. It reduces duplicate or early runs.

## Folder

Use this trigger when files inside a folder should start a flow.

Parameters:

```txt
Folder path        Folder to watch
Change type        File created, File modified, File deleted, or Any change
File name filter   Optional wildcard filter
Include subfolders Watch nested folders too
Debounce seconds   Wait time before firing after a change
```

Example:

```txt
Folder path: C:\Input
Change type: File created
File name filter: *.pdf
Include subfolders: off
Debounce seconds: 2
```

Typical use:

1. Watch an intake folder.
2. Filter to the file type the flow can process.
3. Keep subfolders off unless the intake location is organized by customer, date, or source.

## Queue

Use this trigger when queue work should start a flow.

Parameters:

```txt
Queue name             Queue to monitor
Item status            Blank, In Progress, Failed, or Any
Minimum items          Number of matching items needed before firing
Poll interval seconds  How often the queue should be checked
```

Typical use:

1. Create a queue in `Queue Management`.
2. Add work items to the queue.
3. Add a Queue trigger with `Item status` set to `Blank`.
4. In the flow, use `Queue > Get Next Item`.
5. After processing, use `Queue > Update Item`.

For most queue-driven flows, use:

```txt
Item status: Blank
Minimum items: 1
Poll interval seconds: 30
```

## Webhook

Use this trigger when another system sends an event notification to Likha.

Parameters:

```txt
Webhook URL          Generated URL for the external system
Relative path        Optional custom path
Secret token         Optional shared token for verification
Event name           Optional event filter
Payload JSON Schema  Optional expected payload shape
```

Example payload schema:

```json
{
  "type": "object",
  "properties": {
    "event": {
      "type": "string"
    },
    "record_id": {
      "type": "string"
    }
  }
}
```

Typical use:

1. Add the trigger.
2. Copy the generated `Webhook URL`.
3. Paste it into the external application webhook settings.
4. Set a `Secret token` if the sender supports shared secrets.
5. Set `Event name` if the sender uses one URL for multiple event types.

## Windows Event

Use this trigger when a Windows Event Log entry should start a flow.

Parameters:

```txt
Log name                    Application, System, Security, or Setup
Source                      Optional event source
Event ID                    Optional numeric event ID
Level                       Any, Error, Warning, or Information
Keywords / message contains Optional text match
```

Example:

```txt
Log name: Application
Source: MsiInstaller
Event ID: 1033
Level: Information
Keywords / message contains: completed
```

Typical use:

1. Choose the Windows log to monitor.
2. Add a source or event ID to avoid firing on unrelated events.
3. Use message keywords for extra filtering.

## Recommended trigger design

Use narrow filters whenever possible.

Good examples:

```txt
Folder path: C:\Input\Invoices
File name filter: *.pdf

Queue name: InvoiceQueue
Item status: Blank

Email address: ap@example.com
Subject contains: Invoice
Only when attachments exist: on
```

Avoid broad triggers unless the flow can safely handle many events:

```txt
Folder path: C:\
Change type: Any change

Email address: shared@example.com
Folder: Inbox
No filters
```

## Testing a trigger definition

After saving a trigger:

1. Confirm it appears under `Robots > Event triggers`.
2. Confirm the trigger is `Enabled`.
3. Confirm the target flow runs successfully from `Run now`.
4. Create the matching event, such as adding a file, queue item, email, or webhook request.
5. Check `Runs & Logs` and `Robots > Robot jobs`.

## Troubleshooting

If a trigger does not fire:

- Confirm the trigger is enabled.
- Confirm the selected flow still exists.
- Confirm `LikhaRobotService` is running.
- Confirm `LikhaUserAgent` is running for browser, desktop, mouse, keyboard, or screen automation.
- Confirm file and folder paths exist on the machine that watches them.
- Confirm queue names match exactly.
- Confirm webhook callers can reach the Control Room URL.
- Confirm Windows Event filters are not too narrow.

For VM robot setups, also confirm the robot can reach the Control Room server and shows as Online in:

```txt
Robots
```
