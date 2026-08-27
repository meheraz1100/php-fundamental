# If, Else, and Elseif

`if`, `elseif`, and `else` let you choose which block of code runs based on a condition. PHP checks the branches from top to bottom and runs the first one that matches.

Use `if` for the first check, `elseif` for additional checks, and `else` for the fallback case when nothing else matches.

## Example

```php
<?php
$score = 82;

if ($score >= 90) {
    echo "Grade: A" . PHP_EOL;
} elseif ($score >= 80) {
    echo "Grade: B" . PHP_EOL;
} else {
    echo "Grade: C or lower" . PHP_EOL;
}
```

## Expected Output

```text
Grade: B
```

## Tip

Keep your conditions ordered from most specific to most general. Once PHP finds a true branch, it stops checking the rest.
