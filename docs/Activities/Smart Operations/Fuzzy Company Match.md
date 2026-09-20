---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Fuzzy Company Match

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Smart operations

## Purpose

Normalizes company names, removes common legal suffixes, and returns `true` when the names match at or above the configured threshold.

## Properties

- `company_a`: First company name.
- `company_b`: Second company name.
- `cleanup_pattern`: Regex used during company-name normalization. Default: `[^a-z0-9]+`.
- `whitespace_pattern`: Regex used to collapse whitespace. Default: `\s+`.
- `threshold`: Minimum match score.
- `output`: Boolean output variable.

## Example

```txt
company_a: Company A Inc.
company_b: Company A Incorporated
threshold: 88
output: company_match
```

