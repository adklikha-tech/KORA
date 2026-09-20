---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Queue Update Item

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

**Activity group:** Queues

## Purpose

Updates a queue item status and output payload.

## Properties

- `queue`: Queue name.
- `item_id`: Queue item id variable or literal id.
- `status`: New status, such as Success or Failed.
- `output`: JSON output payload.

## Example

```txt
item_id: queue_item_id
status: Success
output: {"processed":true}
```
