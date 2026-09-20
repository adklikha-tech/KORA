---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Browser Select radio button

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Selects a radio button on a web page.

## Properties

- `instance`: BrowserInstance to use.
- `selector`: CSS selector or captured selector for the radio button. Use Pick to capture and Highlight to verify.

## Example

```txt
instance: Browser1
selector: input[name="plan"][value="pro"]
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
