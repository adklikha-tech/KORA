---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Architecture

Likha can run as a single-machine attended studio or as a distributed Agentic Process Automation platform with a Control Room and unattended robot VMs.

The architecture separates decision-making from execution. An agent interprets a goal and selects an approved tool; the workflow engine and robot runtime execute that tool under defined operational controls.

## Core Components

- Agent runtime: manages prompts, session context, knowledge retrieval, flow tools, specialist delegation, guardrails, and completion or escalation decisions.
- Tool and flow registry: exposes only the workflows and specialist agents approved for an agent.
- Desktop shell: `desktop.py`, using pywebview.
- Web app and API: `app/main.py`, using FastAPI.
- Workflow engine: `app/engine.py`.
- Database: SQLite under `data/` by default, or a configured PostgreSQL or Microsoft SQL Server database.
- Designer UI: `static/studio.html`, `static/studio.js`, and CSS.
- Robot service: `app/robot_service.py`.
- User agent: `app/user_agent.py`.
- Remote robot runtime helpers: `app/robot_runtime.py`.

See [Agent Infrastructure](22%20-%20Agent%20Infrastructure.html) for the full agent execution and governance model.

See [Database Settings](Database%20Settings.html) for database requirements, activation, and switching behavior.

## Attended Setup

```text
User workstation
  Likha desktop app
  Process Designer
  Local SQLite database
  Workflow engine
  Browser/Desktop automation in the active user session
```

Use this setup when one user builds and runs workflows on the same machine.

Typical command:

```bat
run_desktop.bat
```

## Unattended Setup

```text
Robot machine
  Likha Control Room
  LikhaRobotService
  LikhaUserAgent
  Selected SQLite, PostgreSQL, or SQL Server database
  Schedules, event triggers, robot jobs
```

Use this setup when schedules, trigger-based runs, or background robot jobs should run without manually clicking Run in the designer.

`LikhaRobotService` supervises schedules and jobs.

`LikhaUserAgent` runs inside the logged-in Windows session for browser, desktop, mouse, keyboard, monitor, and message box activities.

See:

- [Robot Service and User Agent.md](Robot%20Service%20and%20User%20Agent.html)
- [Event Triggers.md](Activities/Event%20Triggers/Event%20Triggers.html)

## Server VM Setup

```text
Control Room server
  Likha Control Room
  Selected SQLite, PostgreSQL, or SQL Server database
  Scheduler
  Queue Management
  Robot jobs
  Logs
  HTTP API

Robot VM 1..N
  LikhaRobotService
  LikhaUserAgent
  Browser/Desktop/Excel/UI automation
```

Use this setup when a central server owns agents, knowledge, conversations, workflows, schedules, queues, robot registrations, and logs while separate VM robots execute jobs. PostgreSQL or Microsoft SQL Server is recommended when multiple Likha services need a shared data store.

See:

[Distributed Control Room and VM Robot Setup.md](Distributed%20Control%20Room%20and%20VM%20Robot%20Setup.html)

## Runtime Rule

Designer Run should execute in the designer. Unattended queueing should happen only when a schedule, event trigger, Control Room job, or unattended robot run requests it.

