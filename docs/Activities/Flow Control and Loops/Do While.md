---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Do While

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Loop

## Purpose

Runs body activities once, then repeats while the operation is true.

## Properties

- `operation`: Boolean expression checked after each iteration.
- `body_steps`: Activities to run.

## Example

```txt
operation: keep_running == true
```
