# Variables

Variables store values that can change while a program runs. In PHP, variable names start with `$` and are case-sensitive. A variable can hold strings, numbers, arrays, objects, or other values.

Variables are created the first time you assign a value to them.

## Example

```php
<?php
$city = "Dhaka";
$temperature = 31;

echo $city . " is " . $temperature . " degrees today." . PHP_EOL;

$temperature = 29;
echo $city . " is now " . $temperature . " degrees." . PHP_EOL;
```

## Expected Output

```text
Dhaka is 31 degrees today.
Dhaka is now 29 degrees.
```

## Tip

Avoid using unclear variable names like `$x` or `$data` when the meaning matters. Clear names make code easier to understand and debug.
