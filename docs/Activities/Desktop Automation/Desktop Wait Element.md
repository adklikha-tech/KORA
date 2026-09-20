---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Desktop Wait Element

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Desktop

## Purpose

Waits for a desktop UI element to appear or disappear.

## Properties

- `selector`: Captured desktop selector.
- `wait_for_element_to`: contains element or not contain element.
- `timeout`: Maximum seconds to wait.
- `output`: Boolean variable.

## Example

```txt
wait_for_element_to: contains element
timeout: 30
output: element_found
If Else operation: element_found == true
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
