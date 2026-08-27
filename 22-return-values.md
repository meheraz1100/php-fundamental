# Return Values

Use `return` to send a result back to the code that called the function. A returned value can be stored, displayed, or used in another expression.

```php
<?php
declare(strict_types=1);

function add(int $left, int $right): int
{
    return $left + $right;
}

$total = add(7, 5);
echo $total . PHP_EOL;
```

Expected output:

```text
12
```

The `: int` declaration says this function returns an integer. `return` immediately ends the function.

Tip: return data from reusable functions instead of echoing it; the caller can then choose how to present it.
