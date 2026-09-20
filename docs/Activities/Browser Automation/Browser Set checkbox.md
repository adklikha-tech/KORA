---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Browser Set checkbox

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Checks or unchecks a checkbox on a web page.

## Properties

- `instance`: BrowserInstance to use.
- `selector`: CSS selector or captured selector for the checkbox. Use Pick to capture and Highlight to verify.
- `checkbox_state`: checked when true, unchecked when false.

## Example

```txt
instance: Browser1
selector: input[name="agree"]
checkbox_state: true
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
