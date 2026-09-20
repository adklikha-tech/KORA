---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

## Queue Management guide

Queue Management lets you store work items in Control Room and process them from flows.

Use queues when you want one or more flows to pick up work from a shared list, process each item, and update the item result.

Common examples:

- Customer records to process
- Invoice numbers to download
- Website accounts to check
- API records to enrich
- Excel rows converted into work items

### Where queues are managed

Open Control Room, then go to:

```txt
Queue Management
```

From there you can:

- Create a queue
- Select a queue
- View queue items
- Filter items by status
- Add queue items manually

Queue item statuses are:

```txt
Blank
In Progress
Success
Failed
```

New queue items are created with a blank status.

### Queue item structure

A queue item has these main fields:

```txt
id          internal queue item ID
queue       queue name
item_key    unique item key
status      current queue item status
payload     JSON data for the work item
```

Example queue item:

```json
{
  "id": 5,
  "queue": "test",
  "item_key": "QI-186-1782595785342",
  "status": "In Progress",
  "payload": {
    "id": 1001,
    "name": "John Doe",
    "email": "john.doe@example.com",
    "active": true
  }
}
```

### Queue > Add Item

`Queue > Add Item` adds a new item to a selected queue.

Properties:

```txt
queue     existing queue selected from Control Room queues
payload   JSON object containing item data
```

The item key is assigned automatically.

The new item status is blank.

Example payload:

```json
{
  "id": 1001,
  "name": "John Doe",
  "email": "john.doe@example.com",
  "active": true
}
```

### Queue > Get Next Item

`Queue > Get Next Item` gets the next blank-status item from the selected queue.

When an item is picked, its status changes to:

```txt
In Progress
```

Properties:

```txt
queue           existing queue selected from Control Room queues
save_as         object variable that stores the full queue item
queue_item_id   Number variable that stores the queue item ID
status          Text variable that stores the current status
```

Default output variables:

```txt
queue_item
queue_item_id
queue_item_status
```

After `Queue > Get Next Item`, the full item is available through the `save_as` variable.

If `save_as` is:

```txt
queue_item
```

Then the values can be referenced like this:

```txt
{{queue_item.id}}
{{queue_item.queue}}
{{queue_item.item_key}}
{{queue_item.status}}
{{queue_item.payload.id}}
{{queue_item.payload.name}}
{{queue_item.payload.email}}
{{queue_item.payload.active}}
```

### Example: output John Doe from queue_item

Given this queue item:

```json
{
  "id": 5,
  "queue": "test",
  "item_key": "QI-186-1782595785342",
  "status": "In Progress",
  "payload": {
    "id": 1001,
    "name": "John Doe",
    "email": "john.doe@example.com",
    "active": true
  }
}
```

Use this syntax to get the name:

```txt
{{queue_item.payload.name}}
```

Example Log activity message:

```txt
Customer name is {{queue_item.payload.name}}
```

Output:

```txt
Customer name is John Doe
```

### Queue > Update Item

`Queue > Update Item` updates a queue item status after processing.

Properties:

```txt
queue     existing queue selected from Control Room queues
item_id   queue item ID to update
status    In Progress, Success, or Failed
output    JSON object containing optional result data
```

Most flows use the queue item ID from `Queue > Get Next Item`.

Example `item_id`:

```txt
queue_item_id
```

Or, if you prefer using the full queue item object:

```txt
queue_item.id
```

Token syntax also works:

```txt
{{queue_item_id}}
{{queue_item.id}}
```

Example success output:

```json
{
  "message": "Customer processed",
  "customer_name": "{{queue_item.payload.name}}"
}
```

### Typical queue workflow

1. Create a queue in Control Room.
2. Add queue items manually or with `Queue > Add Item`.
3. In a process, add `Queue > Get Next Item`.
4. Use payload values in activities.
5. Add `Queue > Update Item`.
6. Set status to `Success` if processing finished.
7. Set status to `Failed` if processing failed.

Example flow:

```txt
Queue > Get Next Item
Log: Processing {{queue_item.payload.name}}
Browser / Desktop / API / Excel activities
Queue > Update Item
```

### Dot notation for payload values

Use dot notation to read values inside the queue item payload.

Examples:

```txt
{{queue_item.payload.id}}
{{queue_item.payload.name}}
{{queue_item.payload.email}}
{{queue_item.payload.active}}
```

For nested payload objects, continue the dot path.

Example payload:

```json
{
  "customer": {
    "name": "John Doe",
    "address": {
      "city": "Manila"
    }
  }
}
```

Syntax:

```txt
{{queue_item.payload.customer.name}}
{{queue_item.payload.customer.address.city}}
```

### Important notes

`Queue > Get Next Item` only picks items with a blank status.

Once picked, the item becomes `In Progress`.

Use `Queue > Update Item` to mark the item as `Success` or `Failed`.

If there are no blank-status items, `Queue > Get Next Item` saves `null` to the `save_as` variable.

For activity fields that expect JSON, keep the value as valid JSON.

Valid:

```json
{
  "name": "{{queue_item.payload.name}}"
}
```

Invalid:

```json
{
  "name": {{queue_item.payload.name}}
}
```
