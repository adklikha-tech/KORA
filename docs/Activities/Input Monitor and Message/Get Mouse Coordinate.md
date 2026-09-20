---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Get Mouse Coordinate

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Mouse and Keyboard

## Purpose

Stores the current mouse pointer coordinates.

## Properties

- `x_output`: Number variable for X coordinate.
- `y_output`: Number variable for Y coordinate.

## Example

```txt
x_output: mouse_x
y_output: mouse_y
Log: {{mouse_x}}, {{mouse_y}}
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
