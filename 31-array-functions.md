# Array Functions

PHP provides functions for inspecting and transforming arrays. Choose functions that return a new array when you do not want to modify the original.

```php
<?php
$numbers = [4, 1, 3];
sort($numbers);

echo count($numbers) . PHP_EOL;
echo implode(', ', $numbers) . PHP_EOL;
```

Expected output:

```text
3
1, 3, 4
```

Common helpers include `count`, `in_array`, `array_keys`, `array_values`, `array_filter`, and `array_map`.

Pitfall: functions like `sort()` mutate the array and return `true` or `false`, not the sorted array.
