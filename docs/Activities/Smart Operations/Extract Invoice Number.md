---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Extract Invoice Number

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Smart operations

## Purpose

Uses one or more regex patterns to extract an invoice number from text.

## Properties

- `input`: Text that may contain an invoice number.
- `regex_patterns`: One regex per line. The first capturing group is returned as the invoice number.
- `output`: Text output variable.

## Example

```txt
input: Invoice No. INV-1001 due today
output: invoice_number
```

