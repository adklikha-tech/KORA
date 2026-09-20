---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Run VBScript

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

**Activity group:** Scripting

## Purpose

Runs VBScript code.

## Properties

- `command`: VBScript code.
- `timeout`: Maximum seconds to wait.
- `output`: Standard output variable.
- `script_error`: Standard error variable.

## Example

```txt
command: WScript.Echo "Hello"
output: VBScriptOutput
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
