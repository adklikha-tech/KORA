---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Browser Click Image on Webpage

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Clicks a captured image or visual element on a webpage.

## Properties

- `instance`: BrowserInstance to use.
- `image_name`: Name for the captured image.
- `image_data`: Captured image data.
- `confidence`: Image match confidence.
- `click_action`: left click, right click, or double click.
- `click_type`: background or hardware.

## Example

```txt
instance: Browser1
image_name: login_button
confidence: 0.95
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
