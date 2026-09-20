---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Get Last Row Column Excel

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Excel

## Purpose

Finds the last used row and column in a worksheet.

## Properties

- `instance`: ExcelInstance to inspect.
- `sheet_name`: Worksheet name.
- `last_row_output`: Number variable for last row.
- `last_column_output`: Number variable for last column.

## Example

```txt
last_row_output: LastRow
last_column_output: LastColumn
If Else operation: LastRow > 1
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
