---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Go To

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Flow control

## Purpose

Jumps execution to a Label in the same flow section.

## Properties

- `target_label`: Label name to jump to.

## Example

```txt
target_label: cleanup
```
