---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Insert Column

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Data Table

## Purpose

Adds a column to an existing DataTable/List variable.

## Properties

- `data_table`: DataTable/List variable to update.
- `column_name`: Column name to add.

## Notes

For row-object DataTables, the new column is added with an empty value on each row. For list rows, an empty value is appended to each row.
