# Indexed Arrays

An indexed array stores values under numeric positions starting at `0`. Use it for an ordered list.

```php
<?php
$colors = ['red', 'green', 'blue'];

echo $colors[0] . PHP_EOL;
print_r($colors);
```

Expected output starts with:

```text
red
Array
(
    [0] => red
```

Add an item with `$colors[] = 'yellow';` or replace a position with `$colors[1] = 'lime';`.

Pitfall: accessing an index that does not exist produces a warning. Check with `array_key_exists()` when input may be incomplete.
