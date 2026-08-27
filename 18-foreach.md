# Foreach

`foreach` loops over arrays and other traversable values one item at a time. It is the clearest way to read every value in a collection.

You can loop over just the values, or over both keys and values when the array is associative.

## Example

```php
<?php
$scores = [
    "Ava" => 95,
    "Noah" => 87,
    "Mia" => 91,
];

foreach ($scores as $name => $score) {
    echo $name . ": " . $score . PHP_EOL;
}
```

## Expected Output

```text
Ava: 95
Noah: 87
Mia: 91
```

## Tip

`foreach` is usually easier to read than manual index loops. If you iterate by reference, be careful not to reuse the reference variable accidentally after the loop.
