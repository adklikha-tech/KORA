---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Normalize Text

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Smart operations

## Purpose

Converts text into a cleaner comparison-friendly value by lowercasing, replacing unwanted characters, and collapsing whitespace.

## Properties

- `input`: Text to normalize.
- `cleanup_pattern`: Regex used to replace non-normalized text. Default: `[^a-z0-9]+`.
- `whitespace_pattern`: Regex used to collapse whitespace. Default: `\s+`.
- `output`: Text output variable.

## Example

```txt
input: ACME, Inc.
output: normalized_text
```

