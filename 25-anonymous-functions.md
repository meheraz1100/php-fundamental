# Anonymous Functions

An anonymous function has no declared name. Store it in a variable or pass it as a callback when a small piece of behavior is needed once.

```php
<?php
$double = function (int $number): int {
    return $number * 2;
};

echo $double(6) . PHP_EOL;
```

Expected output:

```text
12
```

To read an outer variable, explicitly import it: `function () use ($name) { ... }`. Imported values are copied unless imported by reference with `&`.

Pitfall: remember the semicolon after the closing `};` when assigning an anonymous function to a variable.
