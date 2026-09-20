---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

# Operations

![Likha Process Designer](../../images/process-designer.png)

Operations are expressions that can read variables directly by name. Do not wrap variables with `{{ }}` inside operation fields.

## Activities with operations

- `Data > Set Variable`: calculates a value and stores it in the selected variable.
- `Conditional > If Else`: runs Then when the operation returns true; otherwise runs Else.
- `Conditional > Case`: each case block has its own operation. The first true case runs.
- `Loop > Loop`: Start From, End To, and Increment By are number operations.
- `Loop > Do while`: runs the body once, then repeats while the operation returns true.

## Basic syntax

```txt
count + 1
price * quantity
(total + tax) / 2
status == "Done"
element_found AND is_ready
NOT has_error
current_row["Last Name"]
```

Use `AND`, `OR`, and `NOT` for boolean logic. Comparisons support `==`, `!=`, `>`, `>=`, `<`, and `<=`.

## Number operations

- Add: `left + right` or `add(left, right)`
- Subtract: `left - right` or `subtract(left, right)`
- Multiply: `left * right` or `multiply(left, right)`
- Divide: `left / right` or `divide(left, right)`
- Round: `round(value, digits)`
- Ceiling: `ceiling(value)` or `ceil(value)`
- Floor: `floor(value)`
- Truncate: `truncate(value)`
- Absolute Value: `absolute_value(value)` or `abs(value)`
- Percentage: `percentage(value, percent)`
- Format Number: `format_number(value, decimals)`
- Format Currency: `format_currency(value, symbol, decimals)`
- Parse Number: `parse_number(text)`
- Is Numeric: `is_numeric(value)`
- Is Even/Odd: `is_even(value)` or `is_odd(value)`
- Random Number: `random_number()`
- Random Integer: `random_integer(minimum, maximum)`
- Random Decimal: `random_decimal(minimum, maximum)`
- Random Number in Range: `random_number_in_range(minimum, maximum)`
- Sum: `sum(value1, value2, value3)` or `sum([value1, value2, value3])`
- Average: `average(value1, value2, value3)` or `average([value1, value2, value3])`
- Min/Max: `min(value1, value2)` and `max(value1, value2)`
- Compare Numbers: `compare_numbers(left, right)` returns `-1`, `0`, or `1`
- Extract Digits: `extract_digits(text)`
- Remove Digits: `remove_digits(text)`
- Extract Decimal Number: `extract_decimal_number(text)`

## String operations

- Concatenate: `concatenate(value1, value2)` or `concat(value1, value2)`
- Split: `split(text, delimiter)` returns a list.
- Join: `join(list_value, delimiter)`
- Replace: `replace(text, old_text, new_text)`
- Trim: `trim(text)`
- Length: `length(text)`
- Left: `left(text, count)`
- Right: `right(text, count)`
- Substring: `substring(text, start, end)`
- Extract Between: `extract_between(text, start_text, end_text)`
- Contains: `contains(text, search_text)`
- Starts With: `starts_with(text, prefix)`
- Ends With: `ends_with(text, suffix)`
- To Uppercase: `to_uppercase(text)` or `upper(text)`
- To Lowercase: `to_lowercase(text)` or `lower(text)`
- Title Case: `title_case(text)`
- Pad Left: `pad_left(text, width, fill_character)`
- Pad Right: `pad_right(text, width, fill_character)`
- Regex Match: `regex_match(text, pattern)`
- Regex Replace: `regex_replace(text, pattern, replacement)`
- Remove Digits: `remove_digits(text)`
- Remove Symbols: `remove_symbols(text)`
- Base64 Encode: `base64_encode(text)`
- Base64 Decode: `base64_decode(text)`
- Is Empty: `is_empty(text)`
- Clean Text: `clean_text(text)`

## Examples

```txt
name: total
operation: add(price, tax)
```

```txt
name: rounded_total
operation: round(total, 2)
```

```txt
name: invoice_digits
operation: extract_digits(invoice_text)
```

```txt
name: customer_name
operation: title_case(trim(raw_customer_name))
```

```txt
name: order_id
operation: extract_between(message, "Order ", " is ready")
```

```txt
name: phone_digits
operation: regex_replace(phone_text, "[^0-9]", "")
```

```txt
If Else operation: is_numeric(total_text) AND parse_number(total_text) > 0
```

```txt
If Else operation: starts_with(email, "admin") OR is_empty(email)
```

```txt
Case operation: compare_numbers(balance, 0) < 0
```

```txt
Loop Start From: 1
Loop End To: total_rows - 1
Loop Increment By: max(step_size, 1)
```
