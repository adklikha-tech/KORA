---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Browser Extract Text

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Reads text from a web element into a variable.

## Properties

- `instance`: BrowserInstance to use.
- `selector`: CSS selector or captured selector.
- `save_as`: Text variable to store extracted text.

## Example

```txt
selector: h1
save_as: page_title
Log: {{page_title}}
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
