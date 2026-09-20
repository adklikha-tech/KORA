---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Desktop Click

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Desktop

## Purpose

Clicks a desktop UI element using selector, image/OCR fallback, or coordinates.

## Properties

- `selector`: Captured desktop selector.
- `click_action`: left click, right click, double click, and related actions.
- `click_type`: background or hardware click.
- `fallback_coordinates`: Use x/y if selector fails.
- `fallback_ocr`: Use image/OCR fallback.
- `x`: Fallback X coordinate.
- `y`: Fallback Y coordinate.
- `ocr_text`: Optional text to find with OCR if image matching misses.
- `ocr_image_data`: Captured fallback image.
- `ocr_confidence`: Image matching confidence.

## Fallback order

When OCR/image fallback is enabled, Desktop Click uses it before the selector. This is useful when the selector exists but the reliable target is the captured visual control.

Desktop Click tries selected fallback methods in this order:

1. Captured image match.
2. OCR target text match.
3. X/Y coordinates, only when `fallback_coordinates` is enabled.

Image and OCR fallback are searched inside the picked application window when Likha can identify it, or near the picked desktop element when available. Likha only uses the x/y fallback point when `use x/y fallback` is checked.

If you enable OCR/image fallback, either pick a fallback image, enter OCR target text, or use both.

OCR/image fallback does not click the x/y fallback point unless `use x/y fallback` is also checked.

OCR target text is useful when the button or label text is stable but the image changes because of theme, scaling, focus state, or hover state.

## Example

```txt
selector: {captured selector}
click_action: left click
fallback_ocr: true
ocr_text: Submit
fallback_coordinates: true
x: 100
y: 200
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
