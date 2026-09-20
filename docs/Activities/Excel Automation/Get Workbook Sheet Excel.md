---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Excel > Get Workbook Sheet

![Likha Process Designer](../../images/process-designer.png)

Gets a worksheet name from an open Excel workbook and saves it as text.

## Properties

- **Excel Instance**: The Excel instance variable, for example `Excel1`.
- **Index of the sheet**: 1-based worksheet index. `1` means the first sheet.
- **Use active worksheet**: When checked, returns the active worksheet name and ignores the sheet index.
- **Output Sheet name text**: Text variable that receives the sheet name.

## Output

The selected worksheet name is saved as text.

## Example

Use the active worksheet and save its name to `SheetName`, then use `SheetName` in a later Excel activity.
