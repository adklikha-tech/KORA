---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Browser Extract Table

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Extracts an HTML table into a DataTable variable.

## Properties

- `instance`: BrowserInstance to use.
- `selector`: Table selector.
- `save_as`: DataTable variable to store extracted rows.

## Notes

- Use For Each to loop through the extracted table.
- Use `current_row["Column Name"]` for named columns when rows are objects.

## Example

```txt
selector: table
save_as: orders_dt
For Each source: orders_dt
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
