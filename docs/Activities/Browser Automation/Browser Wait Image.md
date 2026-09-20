---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Browser Wait for Image

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Waits until a captured image appears on a webpage.

## Properties

- `instance`: BrowserInstance to use.
- `image_name`: Name for the captured image.
- `image_data`: Captured image data.
- `confidence`: Image match confidence.
- `timeout`: Maximum seconds to wait.
- `output`: Boolean variable set to true or false.

## Example

```txt
timeout: 30
output: image_found
If Else operation: image_found == true
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
