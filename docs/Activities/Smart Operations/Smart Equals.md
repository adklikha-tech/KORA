---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Smart Equals

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Smart operations

## Purpose

Normalizes two text values, compares them with fuzzy matching, and returns `true` when the score is greater than or equal to the threshold.

## Properties

- `text_a`: First text value.
- `text_b`: Second text value.
- `cleanup_pattern`: Regex used to replace non-normalized text. Default: `[^a-z0-9]+`.
- `whitespace_pattern`: Regex used to collapse whitespace. Default: `\s+`.
- `threshold`: Minimum match score.
- `output`: Boolean output variable.

## Example

```txt
text_a: {{customer_name}}
text_b: Acme Incorporated
threshold: 90
output: customer_matches
```

