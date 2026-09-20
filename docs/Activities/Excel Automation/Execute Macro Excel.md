---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Excel > Execute Macro

![Likha Process Designer](../../images/process-designer.png)

Runs a VBA macro from an open Excel instance and saves the macro return value as text.

## Properties

- **Excel Instance**: The Excel instance variable, for example `Excel1`.
- **Macro name**: The macro to run, for example `Module1.MyMacro` or `Book1.xlsm!Module1.MyMacro`.
- **Macro parameters**: Optional parameters. Use a JSON array such as `["ABC", 123]`, or one parameter per line.
- **Macro output**: Text variable that receives the macro return value.

## Notes

This activity requires Microsoft Excel through COM automation. It runs against an open Excel instance created by **Excel > Launch Excel**.

If the macro does not return a value, the macro output variable is saved as an empty string.
