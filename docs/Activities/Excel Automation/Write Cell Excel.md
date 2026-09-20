---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Write Cell Excel

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Excel

## Purpose

Writes a single value into one Excel cell.

## Properties

- `instance`: ExcelInstance to write to.
- `cell`: Target cell, such as B2.
- `sheet_name`: Worksheet name.
- `input_text`: Text/value to write. Supports variables.

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
cell: B2
input_text: {{current_row["Last Name"]}}
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
