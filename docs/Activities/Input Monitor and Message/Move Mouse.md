---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Move Mouse

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Mouse and Keyboard

## Purpose

Moves the mouse and optionally clicks.

## Properties

- `x`: Screen X coordinate.
- `y`: Screen Y coordinate.
- `send_click`: Whether to click after moving.
- `click_type`: Click type.
- `wait`: Seconds to wait.

## Example

```txt
x: 100
y: 200
send_click: true
click_type: Left click
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
