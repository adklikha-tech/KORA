---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Delete File

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

**Activity group:** File Actions

## Purpose

Deletes a file.

## Properties

- `file_path`: File to delete.
- `output`: Boolean result variable.

## Example

```txt
file_path: C:\Temp\old.txt
output: DeletedFile
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
