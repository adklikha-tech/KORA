---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Desktop Hotkey

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Desktop

## Purpose

Sends a hotkey to a desktop UI target.

## Properties

- `selector`: Captured desktop selector.
- `keys`: Key combination list or text, such as ctrl+s.
- `fallback_coordinates`: Use x/y if selector fails.
- `fallback_ocr`: Use image/OCR fallback.

## Example

```txt
keys: ctrl+s
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
