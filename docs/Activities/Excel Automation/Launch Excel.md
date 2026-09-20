---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Launch Excel

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Excel

## Purpose

Creates or opens an Excel workbook and stores an ExcelInstance variable.

## Properties

- `document_type`: From a Blank Document or Open an Excel File.
- `file_path`: Path when opening an existing file.
- `visible`: Show Excel while running.
- `instance`: ExcelInstance output variable.

## Example

```txt
document_type: Open an Excel File
file_path: C:\Reports\input.xlsx
instance: Excel1
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
