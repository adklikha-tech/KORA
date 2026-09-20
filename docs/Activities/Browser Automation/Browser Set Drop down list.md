---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Browser Set Drop down list

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Selects one or more options in a browser drop down list.

## Properties

- `instance`: BrowserInstance to use.
- `selector`: CSS selector for the drop down list. Use Pick to capture an element and Highlight to verify it.
- `option_names`: Option label, text, or value to select. Use one option per line, or comma-separated values.
- `use_regex`: Treat option names as regular expression patterns.

## Example

```txt
instance: Browser1
selector: select#country
option_names: Singapore
use_regex: false
```

## Regex example

```txt
option_names: ^Sing
use_regex: true
```
