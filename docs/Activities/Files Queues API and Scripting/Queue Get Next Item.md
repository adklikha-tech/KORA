---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# Queue Get Next Item

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

**Activity group:** Queues

## Purpose

Gets the next item from a queue and stores item details in variables.

## Properties

- `queue`: Queue name.
- `save_as`: Object variable for queue item.
- `queue_item_id`: Number variable for item id.
- `status`: Text variable for item status.

## Notes

- Payload fields can be read with `queue_item.payload.Name` or `queue_item.payload["Last Name"]`.

## Example

```txt
save_as: queue_item
Log: {{queue_item.payload["Last Name"]}}
```
