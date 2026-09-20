---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Integration

Likha AI activities use Control Room AI Settings. This lets users bring their own provider, endpoint, key, model, and request settings.

Likha supports a Bring Your Own Key model for AI features. This means each user or company connects their own AI provider account instead of sharing a central Likha-owned AI subscription.

These settings also power Likha Agents. An agent can use the configured model for goal interpretation, context-aware decisions, and tool selection while the Likha runtime performs approved automation actions.

![Likha Control Room - AI Settings](images/control-room-ai-settings.png)

## What This Is For

AI Settings are used by AI-powered activities inside Likha, including:

- AI Prompt
- AI Vision
- AI Table Extract
- AI Extract Document Fields
- AI Knowledge Search
- AI Understand Screen
- AI Find Element
- AI Click
- AI Type into Text field
- AI Read Screen
- AI Verify Screen
- AI Extract Details From
- Likha Copilot, when enabled

Once configured, these activities can reuse the same provider endpoint, API key, model, temperature, and token settings.

## Why Bring Your Own Key

Bring Your Own Key gives customers control over:

- AI provider choice
- API usage cost
- model selection
- data handling policies
- provider billing
- organization-level access controls

Likha does not need to resell AI credits for this mode. The customer pays their AI provider directly.

## Supported Provider Type

The current AI Settings screen supports OpenAI-compatible chat completion endpoints.

Example endpoint:

```text
https://api.openai.com/v1/chat/completions
```

## AI Activities

- [AI Capabilities.md](Activities/AI%20Capabilities/AI%20Capabilities.html)
- [AI Prompt.md](Activities/AI%20Capabilities/AI%20Prompt.html)
- [AI Extract Documents Fields.md](Activities/AI%20Capabilities/AI%20Extract%20Documents%20Fields.html)
- [AI Vision.md](Activities/AI%20Capabilities/AI%20Vision.html)
- [AI Table Extract.md](Activities/AI%20Capabilities/AI%20Table%20Extract.html)
- [AI Knowledge Search RAG.md](Activities/AI%20Capabilities/AI%20Knowledge%20Search%20RAG.html)

## AI Screen Control Activities

AI Screen Control uses a vision-capable model together with screenshots, OCR, and Windows UI information to understand and operate visible applications through natural-language instructions.

- [AI Screen Control overview](Activities/AI%20Screen%20Control/README.html)
- [AI Understand Screen](Activities/AI%20Screen%20Control/AI%20Understand%20Screen.html)
- [AI Find Element](Activities/AI%20Screen%20Control/AI%20Find%20Element.html)
- [AI Click](Activities/AI%20Screen%20Control/AI%20Click.html)
- [AI Type into Text field](Activities/AI%20Screen%20Control/AI%20Type%20into%20Text%20field.html)
- [AI Read Screen](Activities/AI%20Screen%20Control/AI%20Read%20Screen.html)
- [AI Verify Screen](Activities/AI%20Screen%20Control/AI%20Verify%20Screen.html)
- [AI Extract Details From](Activities/AI%20Screen%20Control/AI%20Extract%20Details%20From.html)

Keep the target application visible and unlocked. In unattended or VM execution, the Likha User Agent must run inside the active Windows user session.

## Smart Rule-Based Operations

Smart operations are not provider-based AI calls. They are local rule, regex, and fuzzy matching helpers.

- [Smart Operations](Activities/Smart%20Operations/README.html)

## Configuration

Open:

```text
Control Room > AI Settings
```

Configure:

- Provider
- Endpoint URL
- API key
- Model
- Temperature
- Max tokens

## Typical Use Cases

- Summarize extracted browser or document text.
- Convert free-form text into structured JSON.
- Classify emails or queue items.
- Extract fields from OCR or document output.
- Analyze screenshots, receipts, charts, barcodes, and QR codes.
- Extract table rows from PDFs or images.
- Ask questions from a policy, SOP, folder, or link.
- Understand the controls, forms, tables, and text visible on an application screen.
- Find, click, and type into UI elements described in natural language.
- Verify that an expected screen or application state is visible.
- Extract a named set of details from a visible application into a structured Object with AI Extract Details From.

## Agents and AI Activities

AI activities perform focused tasks inside a workflow. A Likha Agent operates at a higher level: it receives a goal, uses context to select from approved workflows or activities, observes each result, and decides whether to continue, finish, or ask for human input.

The current Agent Builder supports knowledge-base retrieval and citations, per-agent model settings, version history, declared flow inputs and outputs, specialist-agent delegation, deterministic guardrails, a test playground, and locally published embedded chat.

See:

- [Agentic AI and Likha Agents](21%20-%20Agents.html)
- [Agent Infrastructure](22%20-%20Agent%20Infrastructure.html)

## Notes

Do not hard-code API keys inside workflow steps. Use Control Room AI Settings or secured environment configuration.

