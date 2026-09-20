---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Call Flow

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Flow control

## Purpose

Runs another saved workflow from the current workflow.

## Properties

- `workflow`: Workflow id or selected workflow.
- `inputs`: JSON object passed to child flow.
- `outputs`: Mapping from child output names to parent variable names.

## Example

```txt
workflow: Customer Lookup
inputs: {"customer_id":"{{customer_id}}"}
outputs: {"customer_name":"name_from_child"}
```
