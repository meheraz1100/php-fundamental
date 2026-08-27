# Arrow Functions

Arrow functions are short anonymous functions written with `fn`. Their expression is returned automatically, and they automatically capture variables from the surrounding scope by value.

```php
<?php
$taxRate = 0.15;
$addTax = fn(float $price): float => $price * (1 + $taxRate);

echo $addTax(100.0) . PHP_EOL;
```

Expected output:

```text
115
```

Use arrow functions for one-expression callbacks, such as transforming an array with `array_map`.

Tip: use a normal anonymous function when the body needs several statements, loops, or explicit reference capture.
