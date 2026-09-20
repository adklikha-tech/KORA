---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Extract Details From

**Activity group:** AI Screen Control

Extracts user-specified details from the selected application screen and saves them as a structured Object. The activity uses the vision model configured in Control Room AI Settings and sends a screenshot of the target window to that provider. Likha's own interface is excluded from the captured analysis area.

## Properties

- **Target Window:** `Automatic` selects the topmost visible non-Likha application. Enter part of a window title to select a specific application.
- **What to Extract:** Explain the details to extract and the preferred field names or structure. Variables such as `{{RequestedFields}}` can be used.
- **Output Object:** Object containing the extracted details; default `ExtractedDetails`. Requested details that are not visible are returned as `null`.
- **StatusCode output:** AI provider HTTP status; default `AIExtractDetailsStatusCode`.
- **Timeout:** Maximum AI request time in seconds; default `90`.
- **Retry, Retry Count, Retry Interval, and On Error:** Standard execution and failure behavior.

## Example

Example **What to Extract**:

```text
Extract the customer name, account number, current balance, and payment due date.
```

Example output:

```json
{
  "customer_name": "Ada Lovelace",
  "account_number": "A-1042",
  "current_balance": "$1,250.00",
  "payment_due_date": "2026-07-31"
}
```

## Recommended Use

1. Keep the target application visible and unlocked.
2. Specify only the details needed by the next workflow or agent step.
3. Store the result in an Object variable.
4. Validate required fields before using them in a submission, payment, or irreversible action.
5. Use [AI Verify Screen](AI%20Verify%20Screen.html) when the flow must confirm the application state after an action.

Use [AI Read Screen](AI%20Read%20Screen.html) when you need all visible text and layout. Use **AI Extract Details From** when you need a smaller, named set of values.

