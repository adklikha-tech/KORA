---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Browser Press button on web page

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Presses a button or button-like element on a web page.

## Properties

- `instance`: BrowserInstance to use.
- `selector`: CSS selector or captured selector for the button. Use Pick to capture and Highlight to verify.

## Example

```txt
instance: Browser1
selector: button[type="submit"]
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
