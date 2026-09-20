---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Detect Number Format

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Smart operations

## Purpose

Detects common number formats such as integer, decimal dot, decimal comma, thousands comma, thousands dot, human abbreviated, or currency.

## Properties

- `input`: Text to inspect.
- `integer_pattern`: Pattern for integers.
- `decimal_dot_pattern`: Pattern for decimal values using `.`.
- `decimal_comma_pattern`: Pattern for decimal values using `,`.
- `thousands_comma_pattern`: Pattern for values like `1,234.56`.
- `thousands_dot_pattern`: Pattern for values like `1.234,56`.
- `human_abbreviated_pattern`: Pattern for values like `15k` or `2.5M`.
- `currency_pattern`: Pattern for currency-like values.
- `output`: Text output variable describing the detected format.

## Example

```txt
input: 1,234.56
output: number_format
```

