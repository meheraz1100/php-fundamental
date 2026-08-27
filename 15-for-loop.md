# For Loop

`for` is a counting loop. It is a good fit when you know how many times you want to repeat a block of code.

A `for` loop has three parts: initialization, condition, and update. PHP checks the condition before each iteration.

## Example

```php
<?php
$total = 0;

for ($i = 1; $i <= 5; $i++) {
    $total += $i;
}

echo $total . PHP_EOL;
```

## Expected Output

```text
15
```

## Tip

Keep the loop condition easy to read. If the update step does not move the counter toward the condition becoming false, the loop can run forever.
