---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Browser Wait Element

![Likha Process Designer](../../images/process-designer.png)

**Activity group:** Browser

## Purpose

Waits for a web element to appear or disappear and stores the result in a Boolean variable.

## Properties

- `instance`: BrowserInstance to use.
- `element`: CSS selector or captured selector to wait for.
- `wait_for_web_page_to`: Choose whether the page should contain the element or not contain the element.
- `timeout`: Maximum seconds to wait.
- `output`: Boolean variable set to true or false.

## Variable syntax

Use variables in normal text fields with double braces:

```txt
{{variable_name}}
{{object_name.property}}
```

Use the output variable directly in If Else operations:

```txt
element_found == true
```

## Example

```txt
instance: Browser1
element: #status
wait_for_web_page_to: contains element
timeout: 30
output: element_found
```

## Error handling

Activities that expose retry settings support:

- `retry`: try again when the activity fails.
- `retry_count`: number of retry attempts.
- `retry_interval`: seconds between retries.
- `on_error`: stop, resume next, or go to a label.
- `error_label`: target label when `on_error` is Go To.
