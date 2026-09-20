---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

![Likha Process Designer](../../images/process-designer.png)

## Loop > Skip

Skips the current iteration of the nearest loop and continues with the next iteration.

This activity has no configurable properties.

Use `Skip` inside loop bodies:

- `Loop`
- `Do while`
- `For Each`

At runtime, activities after `Skip` in the current loop body are not executed for that iteration.
