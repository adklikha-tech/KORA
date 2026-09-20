---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Convert Date Time to Text

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Data

## Purpose

Converts a DateTime value into a Text variable using a default or custom format.

## Properties

- `input`: DateTime value or variable name to convert.
- `custom_format`: Optional date/time format used for the output text.
- `output`: Text variable to store the result.

Common format tokens include `yyyy`, `yy`, `MM`, `dd`, `HH`, `hh`, `mm`, `ss`, and `tt`.
