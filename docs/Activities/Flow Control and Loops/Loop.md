---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Loop

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Loop

## Purpose

Repeats body activities over a numeric range.

## Properties

- `start_from`: Starting number operation.
- `end_to`: Ending number operation.
- `increment_by`: Number operation to add each iteration.
- `loop_index`: Number variable for current index.
- `body_steps`: Activities to repeat.

Start From, End To, and Increment By can use math operations and Number variables directly.

## Example

```txt
start_from: 1
end_to: total_rows - 1
increment_by: add(step_size, 1)
loop_index: i
Log: {{i}}
```
