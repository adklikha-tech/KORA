---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Run DOS Command

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

**Activity group:** Scripting

## Purpose

Runs a Windows command prompt command.

## Properties

- `command`: DOS command text.
- `timeout`: Maximum seconds to wait.
- `command_output`: Standard output variable.
- `command_error_output`: Standard error variable.
- `command_exit_code`: Exit code variable.

## Example

```txt
command: echo Hello
command_output: CommandOutput
command_exit_code: CommandExitCode
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
