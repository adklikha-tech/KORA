---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Compare Currency

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Smart operations

## Purpose

Parses two currency-like values and returns `true` when the numeric difference is within the configured tolerance.

## Properties

- `left`: First amount.
- `right`: Second amount.
- `currency_number_pattern`: Regex used to find the numeric amount after symbols, commas, and spaces are stripped. Default: `[-+]?\d+(?:\.\d+)?`.
- `tolerance`: Allowed numeric difference.
- `output`: Boolean output variable.

## Example

```txt
left: $10.00
right: 10
tolerance: 0.01
output: currency_equal
```

