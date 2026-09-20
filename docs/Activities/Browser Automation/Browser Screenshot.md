---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Browser Screenshot

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Saves a screenshot from the browser page.

## Properties

- `instance`: BrowserInstance to use.
- `file`: Output screenshot file path or filename.

## Example

```txt
file: screenshot.png
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
