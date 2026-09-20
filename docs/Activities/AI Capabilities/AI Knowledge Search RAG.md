---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# AI Knowledge Search (RAG)

![Likha Control Room - AI Settings](../../images/control-room-ai-settings.png)

**Activity group:** AI Capabilities

## Purpose

Answers a question using a selected knowledge source. The activity reads a file, folder, or link, selects relevant context, asks the configured AI model, and stores both the answer and source references.

Use this for policy lookups, SOP checks, FAQ answers, contract questions, or document-guided decisions inside a flow.

## Properties

- `source_type`: Knowledge source type. Options are `PDF/Word/File`, `Link`, and `Local Folder`.
- `source_path`: File path when `source_type` is `PDF/Word/File`.
- `source_url`: URL when `source_type` is `Link`.
- `folder_path`: Folder path when `source_type` is `Local Folder`.
- `prompt`: Question to answer from the knowledge source.
- `max_context_chars`: Maximum context characters sent to the model. Default is `30000`.
- `answer_output`: Output variable for the answer text.
- `sources_output`: Output variable for source references used as context.
- `status_code`: Output variable for the HTTP status code.

## Supported Local Files

Knowledge Search can read common text-based files, including:

- `.txt`
- `.md`
- `.csv`
- `.json`
- `.html`
- `.htm`
- `.pdf`
- `.docx`

## Example

```txt
source_type: PDF/Word/File
source_path: C:\Policies\expense-policy.pdf
prompt: What is the approval limit for travel expenses?
answer_output: AIKnowledgeAnswer
sources_output: AIKnowledgeSources
status_code: AIKnowledgeStatusCode
```

## Notes

The activity is designed to answer using only the selected knowledge source. If the answer is not available in the source, the model is instructed to say that it is not available.

