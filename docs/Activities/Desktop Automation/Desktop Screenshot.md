---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Desktop Screenshot

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Desktop

## Purpose

Captures a screenshot of the full desktop or selected UI element.

## Properties

- `selector`: Optional captured desktop selector.
- `file`: Output screenshot file.
- `fallback_coordinates`: Use x/y fallback if selector fails.

## Example

```txt
selector: {captured selector}
file: desktop.png
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
