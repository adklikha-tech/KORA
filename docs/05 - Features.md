---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Features

Likha delivers Agentic Process Automation by combining deterministic RPA with Agentic AI. Builders can create fixed workflows for predictable processes, goal-driven agents for variable work, or hybrid automations that use both.

## Agents

- Build versioned agents with a system prompt, welcome message, model override, temperature, grounding mode, and session-memory setting.
- Ingest TXT, Markdown, CSV, JSON, HTML, PDF, DOCX, local folders, and HTTPS sources into knowledge bases.
- Retrieve relevant passages and return citations.
- Expose selected flows as typed tools using their declared input and output variables.
- Delegate focused tasks to explicitly allowed specialist agents without sharing the supervisor's full conversation history.
- Block self-calls and circular delegation chains, with configurable call-count and depth limits.
- Test agents in a playground with per-message approval for side-effecting flows.
- Publish a standalone local chat and copy website embed code with allowed-origin settings.
- Preserve versions, sessions, citations, flow traces, delegation traces, and audit events.

See [Agentic AI and Likha Agents](21%20-%20Agents.html).

## Agent Infrastructure

- Agent runtime, knowledge retrieval, approved flow and specialist-agent tools, and structured results.
- Guardrails for input/output length, rate limits, blocked terms, prompt injection, credentials, destinations, flow risk, and approval.
- Control Room queues, jobs, logs, AI settings, database settings, and robot visibility.
- Local, private VM, and distributed robot execution.
- Runtime limits, approval points, credentials, and audit boundaries.
- Active Windows-session execution through Likha User Agent for UI work.

See [Agent Infrastructure](22%20-%20Agent%20Infrastructure.html).

## Process Designer

- Drag or double-click activities into a workflow.
- Edit properties in a right-side properties panel.
- Use variables, loop items, operation expressions, and activity outputs.
- Run flows in designer mode.
- View live logs and output.
- Switch between light and dark themes.
- Resize the Activities, Properties, and Output panels; saved sizes are restored locally.
- Use the refreshed activity search, workflow cards, properties, dialogs, and canvas styling.

## Control Room

- Flows
- Agents and knowledge bases
- Scheduler
- Runs and Logs
- Global Variables
- Queue Management
- Robots
- AI Settings
- Database settings
- Licensing
- Grouped Automation, Operations, and Administration navigation.
- Light and dark themes saved on the local machine.
- Local Runner status with CPU, memory, heartbeat, and current-flow information.

## Database Settings

- SQLite is automatic for new local installations.
- PostgreSQL and Supabase connection URLs are supported for shared deployments.
- Microsoft SQL Server supports Windows Authentication or SQL Login through ODBC Driver 18.
- Connection testing is available before saving.
- PostgreSQL URLs and SQL Login passwords are encrypted with a key local to the Likha installation.
- Changing the selected database takes effect after restart and does not migrate existing records.

See [Database Settings](Database%20Settings.html).

## Automation Capabilities

- Desktop automation
- Browser automation
- Excel automation
- Data tables
- File actions
- API requests
- Scripting
- Queues
- Mouse and keyboard
- Message boxes
- Monitor control
- Flow control
- AI activities
- AI Screen Control
- Smart rule-based operations
- System activities
- Event triggers

AI Screen Control includes **AI Extract Details From** for returning a requested set of visible screen values as structured data. The extraction instruction accepts workflow variables, and missing requested values are returned as `null`.

## Runtime Capabilities

- Attended designer runs.
- Local unattended service and user agent.
- Distributed Control Room and VM robots.
- Robot job queue and heartbeats.
- Logs and output variables.

## Existing Activity Guides

The detailed activity pages remain in this folder and are linked from the grouped activity documentation pages.

## Activity Documentation Structure

```text
Documentation/
  Activities/
    README.md
    Desktop Automation/
      README.md
    Browser Automation/
      README.md
    AI Capabilities/
      README.md
    AI Screen Control/
      README.md
    Smart Operations/
      README.md
    Excel Automation/
      README.md
    Data and Data Table/
      README.md
    Flow Control and Loops/
      README.md
    Input Monitor and Message/
      README.md
    Files Queues API and Scripting/
      README.md
    Event Triggers/
      README.md
    System/
      README.md
```

Start here:

[Activities/README.md](Activities/README.html)
