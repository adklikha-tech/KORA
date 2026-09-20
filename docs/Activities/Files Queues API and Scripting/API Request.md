---
layout: default
---

<nav class="doc-home-link"><a href="https://burnimjerome.github.io/LIKHA-_-BETA/">&larr; Go back Home</a></nav>

# API Request

![Likha Control Room - Queue Management](../../images/control-room-queues.png)

**Activity group:** API

## Purpose

Sends an HTTP request and stores response variables.

## Properties

- `method`: GET, PUT, DELETE, or POST.
- `url`: Request URL.
- `accept`: Accept header.
- `content_type`: Content-Type header.
- `headers`: JSON object of headers.
- `body`: Request body.
- `username`: Basic auth username.
- `password`: Basic auth password.
- `response`: Response body output variable.
- `response_header`: Response headers output variable.
- `status_code`: HTTP status code output variable.

## Example

```txt
method: POST
url: https://api.example.com/items
headers: {"X-API-Key":"{{api_key}}"}
body: {"name":"Juan"}
status_code: StatusCode
If Else operation: StatusCode == 200
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
