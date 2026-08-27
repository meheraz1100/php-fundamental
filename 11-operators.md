# Operators

Operators perform actions on values. PHP includes arithmetic operators, comparison operators, logical operators, and assignment operators.

The right operator matters. For example, `==` compares values loosely, while `===` compares both value and type.

## Example

```php
<?php
$a = 10;
$b = 3;

echo $a + $b . PHP_EOL;
echo $a % $b . PHP_EOL;
var_dump($a == "10");
var_dump($a === "10");
```

## Expected Output

```text
13
1
bool(true)
bool(false)
```

## Tip

Use strict comparisons like `===` and `!==` when you care about both value and type. That prevents surprising matches such as `10` and `"10"` being treated as equal.
