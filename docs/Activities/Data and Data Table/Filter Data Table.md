---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Filter Data Table

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Data Table

## Purpose

Creates a new DataTable/List variable containing only rows that match one or more filter rules.

## Properties

- `data_table`: Source DataTable/List variable.
- `filters`: Filter rules edited with the Edit button. Each rule has a column, operator, and value.
- `output`: Output DataTable variable.

## Operators

- `equals`
- `not equals`
- `contains`
- `not contains`
- `starts with`
- `ends with`
- `greater than`
- `greater or equal`
- `less than`
- `less or equal`
- `is empty`
- `is not empty`

## Notes

All filter rules must match for a row to be included in the output. For list rows, use `Column1`, `Column2`, or a 1-based numeric column index.
