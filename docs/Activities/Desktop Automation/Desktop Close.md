---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Desktop Close

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Desktop

## Purpose

Closes a desktop window matched by selector.

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
