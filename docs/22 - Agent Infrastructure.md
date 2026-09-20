---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Agent Infrastructure

Agent Infrastructure is the set of Likha services that lets agents use AI, knowledge, specialist agents, and automation flows safely across local workstations, robot machines, and private VM environments.

## Infrastructure Layers

```text
User or business event
  -> Likha Agent (goal, session memory, grounding, planning, tool selection)
  -> Control Room (agent versions, guardrails, knowledge, flows, queues, jobs, logs, AI and database settings)
  -> Workflow engine (validated activity execution)
  -> Robot service and user agent (machine and Windows-session execution)
  -> Desktop apps, browsers, Excel, files, APIs, and enterprise systems
```

## Core Components

- **Agent runtime:** interprets the objective, manages session context, retrieves grounded knowledge, selects enabled flow or specialist-agent tools, and evaluates results.
- **Agent Builder:** manages prompts, versions, model settings, grounding, memory, citations, tool permissions, delegation limits, guardrails, and local publishing.
- **Knowledge bases:** ingest TXT, Markdown, CSV, JSON, HTML, PDF, DOCX, local folders, and HTTPS sources for passage retrieval and citations.
- **Tool and flow registry:** exposes only the flows and specialist agents explicitly approved for an agent.
- **Guardrails:** apply deterministic input, output, rate, prompt-injection, secret, destination, risk, and approval checks around agent work.
- **Control Room:** manages agents, flows, schedules, queues, robot jobs, global variables, logs, AI settings, database settings, and licensing.
- **Workflow engine:** executes deterministic activities and returns structured outputs to the agent.
- **Robot service:** receives and supervises unattended work on a robot machine.
- **Likha User Agent:** performs browser, desktop, mouse, keyboard, monitor, message, and AI Screen Control work inside the active Windows user session.
- **AI provider connection:** supplies the configured model through the Bring Your Own Key settings.
- **Selected database:** stores agents, versions, sessions, knowledge, delegations, guardrail events, workflows, jobs, logs, queues, and settings in SQLite, PostgreSQL, or Microsoft SQL Server.
- **Operational records:** preserve job state, logs, outputs, errors, citations, tool traces, delegation traces, guardrail events, and queue status for monitoring and audit.

## Deployment Models

### Local

The agent, designer, workflow engine, and SQLite data run on one Windows workstation. This is suitable for building, testing, local embedding, and attended agent-assisted work.

### Private Robot VM

Control Room assigns work to one or more Windows robot VMs. Each UI-capable robot needs an active session with Likha User Agent running.

### Distributed

A central Control Room coordinates agents, shared database records, queues, schedules, flows, logs, and robot jobs while separate machines perform the actual automation. PostgreSQL or Microsoft SQL Server can provide the shared data layer. This keeps planning and governance separate from execution capacity.

## Guardrails

Production agent deployments should define:

- Which flows and activities each agent may use.
- Which machines, applications, files, queues, and APIs are in scope.
- Credential and secret access.
- Maximum steps, retries, runtime, and AI usage.
- Maximum flow calls, specialist-agent calls, and delegation depth.
- Human approval points for sensitive or irreversible actions.
- Prompt-injection handling, secret redaction, and allowed destination rules.
- Logging, retention, and redaction requirements.
- A safe stop and escalation path when the goal cannot be completed.

## Reliability Model

Likha combines adaptive AI decisions with deterministic automation boundaries. Use agent reasoning where the input or screen can vary; use validated activities and flows for actions that must be repeatable. Use verification steps after important UI or data changes, and prefer structured outputs over free-form text between tools.

## Related Documentation

- [Agentic AI and Likha Agents](21%20-%20Agents.html)
- [Distributed Control Room and VM Robot Setup](Distributed%20Control%20Room%20and%20VM%20Robot%20Setup.html)
- [Robot Service and User Agent](Robot%20Service%20and%20User%20Agent.html)
- [Orchestrator](17%20-%20Orchestrator.html)
- [AI Integration](10%20-%20AI%20Integration.html)
- [Database Settings](Database%20Settings.html)
