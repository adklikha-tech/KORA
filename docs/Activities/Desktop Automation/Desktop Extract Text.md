---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Desktop Extract Text

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Desktop

## Purpose

Extracts text from a desktop UI element or fallback image/OCR target.

## Properties

- `selector`: Captured desktop selector.
- `output`: Text variable.
- `fallback_coordinates`: Use x/y fallback if selector fails.
- `fallback_ocr`: Use image/OCR fallback.

## Example

```txt
output: desktop_text
Log: {{desktop_text}}
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
