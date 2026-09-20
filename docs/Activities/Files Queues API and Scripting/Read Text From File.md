---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Read Text From File

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

**Activity group:** File Actions

## Purpose

Reads text from a file into a variable.

## Properties

- `file_path`: File path to read.
- `output`: Text variable.
- `encoding`: System Default, ASCII, Unicode, or UTF-8.

## Example

```txt
file_path: C:\Input\notes.txt
encoding: UTF-8
output: OutputText
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
