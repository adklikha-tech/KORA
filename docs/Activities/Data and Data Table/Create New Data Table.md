---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Create New Data Table

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Data Table

## Purpose

Builds a DataTable variable from rows and columns entered in the table editor.

## Properties

- `output`: DataTable variable name to create.
- `Edit Table`: Opens the table editor window. Add columns, rows, and cell values.

## Notes

- The output is a DataTable/List of row objects.
- Use row values in For Each with `current_row["Column Name"]`.
- Count rows with `length(table_variable)` in Set Variable.

## Example

```txt
output: names_dt
columns: Name, Last Name
row 1: Juan, Dela cruz
For Each item access: current_row["Last Name"]
```
