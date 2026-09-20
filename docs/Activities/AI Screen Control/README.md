---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# AI Screen Control Activities

AI Screen Control uses the configured AI provider, a screenshot of the selected target window, OCR, and Windows UI information to understand, extract information from, and operate visible applications using natural-language instructions.

These activities can be used in ordinary workflows or exposed as tools to a Likha Agent. This gives agents a controlled way to work with legacy or visual applications that do not provide a suitable API or stable selector.

## Activities

- [AI Understand Screen](AI%20Understand%20Screen.html)
- [AI Find Element](AI%20Find%20Element.html)
- [AI Click](AI%20Click.html)
- [AI Type into Text field](AI%20Type%20into%20Text%20field.html)
- [AI Read Screen](AI%20Read%20Screen.html)
- [AI Verify Screen](AI%20Verify%20Screen.html)
- [AI Extract Details From](AI%20Extract%20Details%20From.html)

## Requirements

- Configure a vision-capable model in Control Room > AI Settings.
- Keep the target application visible and unlocked while the activity runs.
- For `Target Window`, use `Automatic` for the topmost visible non-Likha application, or enter part of a window title to lock the activity to that application.
- The Likha User Agent must run inside the active Windows user session for unattended or VM execution.

## Recommended Pattern

1. Use AI Find Element to create an `AIElement` variable.
2. Pass that variable to AI Click or AI Type into Text field.
3. Use AI Verify Screen to confirm the expected result.

Use **AI Extract Details From** when the next step needs a specific set of named values from the visible application. Its **What to Extract** property accepts workflow variables, and requested values that are not visible are returned as `null` in the structured Object.

All activities support Retry, Retry Count, Retry Interval, and On Error behavior. AI calls also expose an HTTP status-code output where applicable.
