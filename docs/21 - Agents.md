---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Agentic AI and Likha Agents

Likha Agents combine an AI model, reusable knowledge, session memory, explicitly approved Likha flows, and controlled specialist-agent delegation. Agents decide when an action is needed; flows remain the deterministic execution boundary.

## Prerequisites

Configure an OpenAI-compatible endpoint, API key, and default model under **Control Room > AI Settings**. An agent may optionally override the default model.

## Create a Knowledge Base

1. Open **Control Room > Agents**.
2. Select **+ Knowledge**.
3. Enter a name and optional description.
4. Select **Browse files** to choose one or multiple files. Selected files are added to Sources automatically. You can also enter a local folder or `https://` URL per line.
5. Select **Save and ingest**.

Supported sources are TXT, Markdown, CSV, JSON, HTML, PDF, and DOCX. Folders are scanned recursively. Likha stores extracted text in the selected Likha database and retrieves the most relevant passages for each message.

## Create an Agent

1. Select **+ Agent**.
2. Define the name, description, system prompt, and welcome message.
3. Choose Strict, Assisted, or no grounding.
4. Select knowledge bases.
5. Select the flows the agent is allowed to call.
6. Optionally select specialist agents under **Allowed agent tools**.
7. Set each flow's risk to Low, Medium, High, or Critical. Keep **Require approval** enabled for flows that change files, applications, messages, or external systems.
8. Configure the agent's **Guardrails**.
9. Save the agent. Every save creates a new agent version.

Agent settings also include a model override, temperature, conversation memory, retrieved-passage count, maximum flow calls, maximum agent calls, delegation depth, and citation requirements.

## Flow Tools and Variables

The Agent Builder reads the selected flow's declared input and output variables. Flow inputs become tool parameters supplied by the model. After the run completes, declared flow outputs are returned to the agent so it can explain the result.

Give flows clear names, descriptions, typed inputs, and declared outputs. An agent cannot call flows that were not selected in its configuration.

## Agent Tools and Delegation

Use **Allowed agent tools** to build a supervisor-and-specialist structure. Only explicitly selected agents are exposed as tools to the supervisor. The supervisor sends a focused task; the specialist runs in a separate conversation session using its own system prompt, knowledge bases, flow permissions, guardrails, and model settings.

The specialist receives the delegated task, not the supervisor's complete conversation history. Its response, citations, flow traces, and nested delegation traces are returned to the supervisor as structured tool data.

Configure these limits per agent:

- **Maximum agent calls:** one to three specialist calls for one message.
- **Delegation depth:** one or two levels below the current supervisor.

Likha blocks self-calls and circular chains. A child agent cannot gain flow or agent permissions from its parent. If a specialist calls a side-effecting flow, the normal per-message approval rule still applies.

Every attempt is written to `agent_delegations` with the parent and child agents, their sessions, the focused task, depth, status, result, citations, nested tool traces, and timestamps.

## Guardrails

Guardrails are deterministic checks around AI calls. They apply to direct chat, locally embedded chat, flow tools, and tasks sent to specialist agents. They run before input is sent to the AI provider, before a selected flow executes, and before the final response is stored and shown.

Configure these rules per agent:

- Enable or disable the guardrail policy.
- Limit input and output length and messages per minute.
- Block selected terms or phrases.
- Allow, record, or block common prompt-injection attempts.
- Allow, redact, or block likely credentials and secrets.
- Restrict web destinations, Windows file locations, and email recipient domains used in flow arguments.
- Always require user approval for flows marked High risk.
- Block flows marked Critical risk, even when message approval is enabled.

Values declared as `SecureString`, and flow fields with credential-like names, are redacted from agent tool traces and AI-visible flow results.

Allowed domain, file-location, and email-domain lists are enforced only when they contain values. Domain entries include their subdomains. Windows file paths use directory boundaries, so allowing `C:\Approved` does not allow a similarly named sibling folder.

Triggered rules are written to `agent_guardrail_events` with the agent, session, phase, rule, action, reason, sanitized preview, and timestamp. Detected credentials are redacted before the event is stored. The latest 100 events are available through `GET /api/agents/{agent_id}/guardrail-events` for audit integrations.

These checks reduce risk but do not replace least-privilege Windows accounts, restricted database credentials, network controls, and careful flow design.

## Grounding Modes

- **Strict:** factual answers must come from retrieved knowledge or successful flow and specialist-agent results. The agent says when the answer is unavailable.
- **Assisted:** retrieved knowledge is preferred, but the model may use general knowledge and should distinguish it.
- **None:** no knowledge restriction is applied.

When citations are enabled, retrieved passages are numbered and returned with their filename or URL.

## Playground and Safeguards

The playground keeps memory only within the current session. Start a new session to clear that conversational context.

Side-effecting and high-risk flows require the **Approve side-effecting flows for this message** checkbox. Approval applies only to the submitted message and is cleared afterward. Critical flows remain blocked when the Critical-flow guardrail is enabled.

An agent can make no more than five flow calls and three specialist-agent calls for one message. Every flow run remains visible in **Runs & Logs**, and agent sessions store responses, citations, flow traces, and delegation traces in the selected Likha database.

## Publish and Embed Locally

1. Save the agent.
2. Open **Publish & Embed locally** in Agent Builder.
3. Choose a public slug and optionally list the website origins allowed to embed it.
4. Select **Publish embed**.
5. Use **Open** to test the standalone chat or **Copy code** to copy the generated script tag.

The embedded page, widget script, conversations, knowledge, and flow runs are served by the current Likha installation. Records use SQLite by default or the PostgreSQL or Microsoft SQL Server database selected under **Control Room > Database**.

An embed URL containing `127.0.0.1` or `localhost` works only on the same computer. For an intranet website, use a Likha machine reachable from that network and its hostname or LAN IP. LAN or internet exposure must be enabled deliberately and protected with HTTPS, authentication, rate limits, Windows Firewall rules, and restricted allowed origins.

## Related Documentation

- [Agent Infrastructure](22%20-%20Agent%20Infrastructure.html)
- [Database Settings](Database%20Settings.html)
- [AI Integration](10%20-%20AI%20Integration.html)
- [AI Screen Control](Activities/AI%20Screen%20Control/README.html)
- [Orchestrator](17%20-%20Orchestrator.html)
