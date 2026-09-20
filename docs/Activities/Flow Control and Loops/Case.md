---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Case

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Conditional

## Purpose

Evaluates case blocks in order and runs the first block whose operation is true.

## Properties

- `cases`: One or more case blocks.
- `operation`: Boolean expression for each case.
- `body_steps`: Activities for a matching case.

## Example

```txt
Case 1 operation: status == "New"
Case 2 operation: status == "Done"
```
