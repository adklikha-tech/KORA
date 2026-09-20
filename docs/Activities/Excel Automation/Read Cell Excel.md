---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Excel > Read Cell

![Likha Process Designer](../../images/process-designer.png)

Reads one cell from an open Excel instance and saves the value as text.

## Properties

- **Excel Instance**: The Excel instance variable, for example `Excel1`.
- **Cell**: The cell address to read, for example `A1`.
- **Sheet name**: The worksheet name. Defaults to `Sheet1`.
- **Output text**: Text variable that receives the cell value.

## Output

The selected cell value is saved as a string. Empty cells return an empty string.

## Example

Read `Sheet1!B2` into `CustomerName`, then use `CustomerName` in another activity.
