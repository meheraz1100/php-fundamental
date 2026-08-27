# Type Declarations

PHP 8+ can declare parameter and return types. With strict types enabled, wrong scalar arguments cause a `TypeError` instead of being silently coerced.

```php
<?php
declare(strict_types=1);

function calculateVat(float $price, float $rate): float
{
    return $price * $rate;
}

echo calculateVat(100.0, 0.15) . PHP_EOL;
```

Expected output:

```text
15
```

Useful built-in types include `int`, `float`, `string`, `bool`, `array`, `object`, `mixed`, `void`, and nullable forms such as `?string`.

Tip: `declare(strict_types=1);` must be the first statement in a PHP file (after the opening tag) to affect calls made from that file.
