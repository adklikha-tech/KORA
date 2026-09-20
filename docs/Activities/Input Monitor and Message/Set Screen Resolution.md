---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Set Screen Resolution

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Monitor

## Purpose

Changes monitor resolution settings.

## Properties

- `monitor_width`: Width in pixels.
- `monitor_height`: Height in pixels.
- `monitor_bit`: Color depth.
- `frequency`: Refresh rate.

## Example

```txt
monitor_width: 1920
monitor_height: 1080
monitor_bit: 32
frequency: 60
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
