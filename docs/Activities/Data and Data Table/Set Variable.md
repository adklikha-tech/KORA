---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Set Variable

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Data

## Purpose

Creates or updates a variable using a literal value or operation expression.

## Properties

- `name`: Variable name to create or update.
- `operation`: Expression to calculate the value. Use direct variable names, not {{ }}.

## Operation syntax

Supported examples:

```txt
"Done"
count + 1
add(count, 1)
price * quantity
round(price * quantity, 2)
format_currency(total, "$", 2)
is_numeric(total_text)
extract_digits(invoice_text)
length(names_dt)
upper(status)
current_row["Last Name"]
```

For object keys with spaces, use bracket access:

```txt
current_row["Last Name"]
```

## Example

```txt
name: row_count
operation: length(names_dt)
```
