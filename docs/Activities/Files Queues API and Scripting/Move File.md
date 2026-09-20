---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Move File

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

**Activity group:** File Actions

## Purpose

Moves a file to another folder.

## Properties

- `file_path`: File to move.
- `destination_folder`: Target folder.
- `output`: Boolean result variable.

## Variable syntax

Use variables in normal text fields with double braces:

```txt
{{variable_name}}
{{object_name.property}}
{{current_row["Column Name"]}}
```

Use direct variable names inside operation fields unless the activity help says otherwise:

```txt
count > 1
status == "Done"
current_row["Last Name"]
```

## Example

```txt
file_path: C:\Input\report.pdf
destination_folder: C:\Archive
output: fileMoved
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
