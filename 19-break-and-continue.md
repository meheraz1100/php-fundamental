# Break and Continue

`break` and `continue` control what happens inside loops. `break` stops the loop immediately, while `continue` skips the rest of the current iteration and moves on to the next one.

In nested loops, they affect the innermost loop by default. You can also pass a number, such as `break 2`, to leave more than one loop level.

## Example

```php
<?php
for ($i = 1; $i <= 5; $i++) {
    if ($i === 3) {
        continue;
    }

    if ($i === 5) {
        break;
    }

    echo $i . PHP_EOL;
}
```

## Expected Output

```text
1
2
4
```

## Tip

Use `continue` to skip bad or unwanted items, and use `break` when you are done processing altogether. In nested loops, be precise about how many levels you want to stop.
