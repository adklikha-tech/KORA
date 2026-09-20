---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Browser Go To

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Navigates a BrowserInstance to a URL.

## Properties

- `instance`: BrowserInstance to use.
- `url`: Target URL. Supports variable placeholders.

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
url: https://example.com/search?q={{query}}
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
