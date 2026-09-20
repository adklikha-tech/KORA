---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Log

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Flow control

## Purpose

Writes a message to the run output log.

## Properties

- `message`: Text to write to the output log. Supports variable placeholders.

## Variable syntax

Use variables in normal text fields with double braces:

```txt
{{variable_name}}
{{object_name.property}}
{{current_row["Column Name"]}}
```

Use direct variable names inside operation fields unless the activity help says otherwise:

```txt
count > 1
status == "Done"
current_row["Last Name"]
```

## Example

```txt
message: Processing {{current_row["Name"]}}
```
