---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Browser Run Javascript Function

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Runs a JavaScript function or expression in the current web page and saves the returned value as text.

## Properties

- `instance`: BrowserInstance to use.
- `javascript_function`: JavaScript function or expression to evaluate in the page.
- `result_text`: Text variable that stores the returned value.

## Example

```txt
instance: Browser1
javascript_function: () => document.title
result_text: page_title
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
