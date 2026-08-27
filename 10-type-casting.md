# Type Casting

Type casting changes a value from one type to another. It is useful when data comes in as a string but you need a number, or when you want a predictable type before doing math or comparisons.

PHP supports simple casts like `(int)`, `(float)`, `(string)`, and `(bool)`.

## Example

```php
<?php
$quantity = "4";
$price = "12.50";

$total = (int) $quantity * (float) $price;

var_dump($quantity);
var_dump((int) $quantity);
var_dump($total);
```

## Expected Output

```text
string(1) "4"
int(4)
float(50)
```

## Tip

Casting can hide bad input. If a value is meant to be numeric, validate it first so you do not silently turn `"12abc"` into an unexpected number.
