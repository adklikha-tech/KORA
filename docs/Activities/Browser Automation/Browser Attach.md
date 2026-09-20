---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Browser Attach

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Attaches Studio to an existing browser window.

## Properties

- `instance`: New BrowserInstance variable name.
- `window_selector`: Captured browser window selector.

## Example

```txt
instance: Browser1
window_selector: {captured window selector}
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
