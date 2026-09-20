---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Insert Row

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Data Table

## Purpose

Adds a new row to an existing DataTable/List variable.

## Properties

- `data_table`: DataTable/List variable to update.
- `values`: New value/s to insert. Use a JSON object for named columns, or a JSON array to map values to existing columns.

## Example

```txt
data_table: invoice_rows
values: {"InvoiceNo":"INV-1001","Total":1250.50}
```

```txt
data_table: invoice_rows
values: ["INV-1001",1250.50]
```

## Notes

When `values` is an array, values are mapped to the first existing row's column names. If the table is empty, columns are named `Column1`, `Column2`, and so on.
