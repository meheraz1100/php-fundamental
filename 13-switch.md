# Switch

`switch` compares one value against several possible cases and runs the matching block. It is useful when one variable can take a few known values, such as a menu choice or a day number.

In PHP, `switch` uses loose comparison, so values that look alike can match even if their types differ. Use `break` to stop after the first match and prevent fall-through.

## Example

```php
<?php
$dayNumber = 3;

switch ($dayNumber) {
    case 1:
        echo "Monday" . PHP_EOL;
        break;
    case 2:
        echo "Tuesday" . PHP_EOL;
        break;
    case 3:
        echo "Wednesday" . PHP_EOL;
        break;
    default:
        echo "Unknown day" . PHP_EOL;
}
```

## Expected Output

```text
Wednesday
```

## Tip

Always add `break` unless you intentionally want fall-through behavior. Without it, PHP keeps running the next case blocks.
