---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Browser Click

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Clicks a web element matched by selector.

## Properties

- `instance`: BrowserInstance to use.
- `selector`: CSS selector or captured selector.
- `click_action`: left click, right click, or double click.
- `click_type`: background or hardware.

## Example

```txt
instance: Browser1
selector: button[type="submit"]
click_action: left click
click_type: background
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
