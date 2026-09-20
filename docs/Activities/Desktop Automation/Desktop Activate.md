---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Desktop Activate

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Desktop

## Purpose

Brings a desktop window matched by selector to the foreground.

## Properties

- `selector`: Captured top-level window selector.

## Example

```txt
selector: {captured window selector}
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
