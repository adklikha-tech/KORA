---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Browser Extract Text OCR

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Runs OCR against a captured webpage image and stores text output.

## Properties

- `instance`: BrowserInstance to use.
- `image_name`: Captured image name.
- `image_data`: Captured image data.
- `language`: OCR language code.
- `output`: Text variable for OCR result.

## Example

```txt
language: eng
output: ocr_text
Log: {{ocr_text}}
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
