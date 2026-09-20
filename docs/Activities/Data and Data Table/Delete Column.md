---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Delete Column

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Data Table

## Purpose

Deletes a column from an existing DataTable/List variable.

## Properties

- `data_table`: DataTable/List variable to update.
- `column`: Column name or 1-based column index to delete.

## Examples

```txt
data_table: invoice_rows
column: Total
```

```txt
data_table: invoice_rows
column: 3
```

## Notes

For object rows, use the column name. For list rows, use a 1-based index or `Column1`, `Column2`, and so on.
