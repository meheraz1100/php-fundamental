# Array Manipulation

Manipulate arrays by adding, removing, merging, or slicing items. Pick an operation that preserves the keys you need.

```php
<?php
$tasks = ['read', 'practice'];
array_push($tasks, 'review');
$first = array_shift($tasks);

echo $first . PHP_EOL;
print_r($tasks);
```

Expected output:

```text
read
Array
(
    [0] => practice
    [1] => review
)
```

`array_push` adds to the end and `array_shift` removes the first item. For a single append, `$tasks[] = 'review';` is simpler.

Tip: use `array_merge()` to combine lists; later string keys overwrite earlier ones.
