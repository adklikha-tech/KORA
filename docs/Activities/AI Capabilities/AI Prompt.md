---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Prompt

![Likha Control Room - AI Settings](../../images/control-room-ai-settings.png)

**Activity group:** AI Capabilities

## Purpose

Sends a prompt using the shared AI Settings from Control Room and stores both the full JSON response and extracted text response.

## Properties

- `system_instruction`: System instruction for the assistant.
- `prompt`: User prompt. Supports variables such as `{{customer_name}}`.
- `response_format`: `text` or `json_object`.
- `json_response`: Output variable for the full parsed JSON response.
- `text_response`: Output variable for the assistant text.
- `status_code`: Output variable for the HTTP status code.

## Example

```txt
system_instruction: Return concise JSON for downstream automation.
prompt: Extract the invoice number and total from {{invoice_text}}
response_format: json_object
json_response: AIJson
text_response: AIText
status_code: AIStatusCode
```

## Notes

Configure provider, endpoint URL, API key, model, temperature, and max tokens in Control Room > AI Settings.

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
