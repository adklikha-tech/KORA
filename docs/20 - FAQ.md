---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# FAQ

## Is Likha only an RPA tool?

No. Likha is an Agentic Process Automation platform, also described as Agentic RPA. Fixed workflows handle predictable, repeatable steps, while Likha Agents can interpret a goal, select approved tools, observe results, and adapt the next action within defined limits.

## What is Agentic Process Automation?

Agentic Process Automation combines AI agents that can reason about a goal with controlled automation workflows that perform the work. In Likha, agents use only approved tools and knowledge, while flows, robots, guardrails, approvals, and logs keep execution reliable and observable.

See [Agentic AI and Likha Agents](21%20-%20Agents.html) and [Agent Infrastructure](22%20-%20Agent%20Infrastructure.html).

## What is the difference between a robot, the Likha User Agent, and a Likha Agent?

- A **robot** is the execution machine or runtime that performs automation jobs.
- **Likha User Agent** is the Windows-session component used for UI-capable unattended execution.
- A **Likha Agent** is the goal-driven AI layer that chooses and coordinates approved tools and workflows.

## Is Likha attended or unattended?

Both. Use the desktop designer for attended building and testing. Use robot service, user agent, schedules, and triggers for unattended execution.

## Why does UI automation need a user session?

Desktop, browser, mouse, keyboard, monitor, and message box actions need an interactive Windows session. On robot VMs, `LikhaUserAgent` must run inside the logged-in robot account.

## Where are flows and runtime data stored?

Likha uses SQLite under `data/` by default in development and `%LOCALAPPDATA%\Likha\data\rpa.db` in the installed desktop app. PostgreSQL/Supabase or Microsoft SQL Server can be selected under **Control Room > Database**.

See [Database Settings](Database%20Settings.html).

## Does switching databases migrate my existing data?

No. Changing the database selection points Likha to another data store after restart. Flows, agents, knowledge, settings, queues, schedules, conversations, and run history remain in the previous database until they are exported or migrated separately.

## How does agent delegation work?

A supervisor can call only the specialist agents explicitly selected under **Allowed agent tools**. A specialist receives a focused task in its own session and keeps its own prompt, knowledge, flow permissions, model settings, and guardrails. Likha blocks self-calls and circular delegation chains.

## How are risky agent actions controlled?

Each flow tool has a Low, Medium, High, or Critical risk level. Guardrails can require per-message approval for High-risk flows and block Critical flows. Other rules can limit rates and message sizes, detect prompt injection, redact secrets, block terms, and restrict web domains, file locations, or email domains.

## How do I run a flow on a schedule?

Create a schedule in Control Room Scheduler. Scheduled runs are unattended jobs.

## How do I process many work items?

Use Queue Management with `Queue > Add Item`, `Queue > Get Next Item`, and `Queue > Update Item`.

See:

[Queue Management.md](Activities/Files%20Queues%20API%20and%20Scripting/Queue%20Management.html)

## How do I connect AI?

Configure Control Room AI Settings, then use AI activities such as AI Prompt.

See:

[AI Prompt.md](Activities/AI%20Capabilities/AI%20Prompt.html)

## Why did Excel blanks appear as None before?

Excel libraries report empty cells as `None`. Likha normalizes Read Range blanks to empty text and removes fully empty rows/trailing columns for cleaner DataTables.

## What should I use for browser selectors?

Prefer stable attributes such as `name`, `data-testid`, `aria-label`, or `placeholder`. Use ID only when it is stable.

## Where do I configure event triggers?

Open:

```text
Control Room > Robots > Event triggers
```

See:

[Event Triggers.md](Activities/Event%20Triggers/Event%20Triggers.html)

