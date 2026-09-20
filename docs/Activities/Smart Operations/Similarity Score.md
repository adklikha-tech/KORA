---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Similarity Score

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Smart operations

## Purpose

Compares two text values and returns a number score from `0` to `100`.

## Properties

- `text_a`: First text value.
- `text_b`: Second text value.
- `method`: Matching method. `rapidfuzz` is used when available, with a local fallback.
- `output`: Number output variable.

## Example

```txt
text_a: Acme Corporation
text_b: Acme Corp.
method: rapidfuzz
output: similarity_score
```

