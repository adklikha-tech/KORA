---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# If Else

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Conditional

## Purpose

Runs Then activities when an operation is true; otherwise runs Else activities.

## Properties

- `operation`: Boolean expression.
- `then_steps`: Activities to run when true.
- `else_steps`: Activities to run when false.

## Operation syntax

Use direct variable names and boolean/comparison operators:

```txt
status == "Done"
row_count > 1
element_found == true
NOT has_error
```

For functions like row counting, first use Set Variable, then compare the result:

```txt
row_count > 1
```

## Example

```txt
operation: row_count > 1
```
