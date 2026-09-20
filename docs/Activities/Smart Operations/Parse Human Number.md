---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Parse Human Number

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Smart operations

## Purpose

Parses human-readable numbers such as `15k`, `2.5M`, or `1 billion` into a numeric output.

## Properties

- `input`: Human-readable number text.
- `number_pattern`: Regex used to find the numeric part. Default: `[-+]?\d+(?:\.\d+)?`.
- `output`: Number output variable.

## Example

```txt
input: 15k
output: parsed_number
```

