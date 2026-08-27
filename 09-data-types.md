# Data Types

PHP supports several data types, including strings, integers, floats, booleans, arrays, null, and objects. Knowing the type helps you predict how values behave in comparisons, output, and calculations.

Use `var_dump()` when you want to see both the value and the type.

## Example

```php
<?php
$name = "Sara";
$age = 21;
$price = 19.99;
$isActive = true;
$tags = ["php", "basics"];
$nothing = null;

var_dump($name, $age, $price, $isActive, $tags, $nothing);
```

## Expected Output

```text
string(4) "Sara"
int(21)
float(19.99)
bool(true)
array(2) {
  [0]=>
  string(3) "php"
  [1]=>
  string(6) "basics"
}
NULL
```

## Tip

PHP will often convert types automatically, but that convenience can hide mistakes. Use strict checks or explicit casting when the type matters.
