---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Write Excel Range

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Excel

## Purpose

Writes a DataTable/List into an Excel sheet.

## Properties

- `instance`: ExcelInstance to write to.
- `starting_cell`: Top-left cell, such as A1.
- `sheet_name`: Worksheet name.
- `input_value`: DataTable/List variable to write.
- `add_headers`: Write object keys as header row.

## Example

```txt
instance: Excel1
starting_cell: A1
input_value: names_dt
add_headers: true
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
