---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Desktop Extract Table

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Desktop

## Purpose

Extracts table-like data from a desktop UI control into a DataTable variable.

## Properties

- `selector`: Captured desktop selector for the table, grid, list, or table container.
- `Pick`: Captures a desktop control and fills the selector.
- `Highlight`: Highlights the currently selected desktop control.
- `Windows selector properties`: Choose which captured Windows properties are used to build the selector.
- `save_as`: DataTable variable that stores the extracted rows.
- `fallback_coordinates`: Use x/y fallback if selector lookup fails.
- `fallback_ocr`: Use image/OCR fallback if selector lookup fails.
- `deep_selector_search`: Search deeper in the UI Automation tree if the fast selector lookup fails.

## Show extracted data

Use **Show extracted Data** after running the process to preview the DataTable saved in `save_as`. The preview uses the same display behavior as Browser > Extract Table.

## Notes

- UI Automation Grid/Table patterns are used when the selected control exposes them.
- If a formal table pattern is not available, the activity tries row-like child controls and then text/OCR parsing.
- Use For Each to loop through the extracted table rows.

## Example

```txt
selector: {"control_type":"TableControl","automation_id":"OrdersGrid"}
save_as: desktop_orders
For Each source: desktop_orders
```

## Error handling

This activity supports:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
