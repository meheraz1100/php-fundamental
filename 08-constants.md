# Constants

Constants hold values that should not change during execution. They are useful for settings, labels, and values that the program should treat as fixed.

Use `define()` or `const` to create constants. Once set, their values cannot be reassigned like normal variables.

## Example

```php
<?php
define("SITE_NAME", "Learn PHP");

const TAX_RATE = 0.15;

$price = 100;
$total = $price + ($price * TAX_RATE);

echo SITE_NAME . PHP_EOL;
echo $total . PHP_EOL;
```

## Expected Output

```text
Learn PHP
115
```

## Tip

Use constants for values that should stay stable across the program, such as app names, configuration flags, or fixed rates.
