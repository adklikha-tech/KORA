---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Browser Start

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Launches a new browser instance for Browser activities.

## Properties

- `instance`: BrowserInstance variable name.
- `browser`: Browser engine, usually chromium or edge.
- `url`: Optional initial URL.
- `headless`: Run without displaying a browser window.
- `keep_open`: Keep browser open after run when visible.

## Variable syntax

Use variables in normal text fields with double braces:

```txt
{{variable_name}}
{{object_name.property}}
{{current_row["Column Name"]}}
```

Use direct variable names inside operation fields unless the activity help says otherwise:

```txt
count > 1
status == "Done"
current_row["Last Name"]
```

## Example

```txt
instance: Browser1
browser: chromium
url: https://example.com
headless: false
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
