---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Read Excel

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Excel

## Purpose

Reads rows from an Excel sheet into a DataTable variable.

## Properties

- `instance`: ExcelInstance to read from.
- `range`: Cell range, or blank for used range.
- `sheet_name`: Worksheet name.
- `add_headers`: Treat first row as column names.
- `output`: DataTable variable.

## Example

```txt
instance: Excel1
sheet_name: Sheet1
range: A1:D10
output: excel_rows
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
