---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Close Excel

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Excel

## Purpose

Closes an ExcelInstance and optionally saves the workbook.

## Properties

- `instance`: ExcelInstance to close.
- `save_option`: Do not save, Save document, or Save document as.
- `document_format`: Format when saving as.
- `document_path`: Path when saving as.

## Example

```txt
instance: Excel1
save_option: Save document as
document_path: C:\Reports\output.xlsx
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
