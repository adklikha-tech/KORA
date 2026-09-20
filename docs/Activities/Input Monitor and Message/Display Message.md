---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Display Message

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Message Boxes

## Purpose

Displays a message box and stores the selected button.

## Properties

- `title`: Message box title.
- `message`: Message body. Supports variables.
- `buttons`: Button set.
- `output`: Text variable for selected button.

## Variable syntax

For `Message box title` and `Message to Display`, you can enter a variable name by itself:

```txt
customer_name
```

This shows the value stored in `customer_name`.

To combine variables with other text, use double braces:

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
title: Confirm
message: Process {{Name}}?
buttons: OKCancel
output: button_selected
```
