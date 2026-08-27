# Do While Loop

`do...while` is like `while`, but it checks the condition after each run. That means the block always executes at least once.

This loop is useful when you need to perform an action first and only then decide whether to repeat it.

## Example

```php
<?php
$count = 5;

do {
    echo "This runs once" . PHP_EOL;
    $count++;
} while ($count < 5);
```

## Expected Output

```text
This runs once
```

## Tip

Use `do...while` when one initial pass is required. A common pitfall is forgetting that it still runs even when the condition is already false.
