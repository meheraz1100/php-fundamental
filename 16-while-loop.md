# While Loop

`while` repeats a block of code as long as a condition stays true. It is useful when you do not know in advance how many iterations you need.

Because the condition is checked before the loop runs, a `while` loop can execute zero times.

## Example

```php
<?php
$count = 3;

while ($count > 0) {
    echo $count . PHP_EOL;
    $count--;
}
```

## Expected Output

```text
3
2
1
```

## Tip

Make sure something inside the loop eventually changes the condition. Without that update, the loop never stops.
