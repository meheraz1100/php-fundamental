# Match

`match` is a PHP 8+ expression that chooses one result from a list of branches. It is similar to `switch`, but it uses strict comparison, returns a value, and does not fall through.

Strict comparison means both value and type must match. For example, `1` and `"1"` are different values in `match`.

## Example

```php
<?php
$code = "404";

$message = match ($code) {
    200 => "OK",
    404 => "Not Found",
    "404" => "Not Found as a string",
    default => "Unknown status",
};

echo $message . PHP_EOL;
```

## Expected Output

```text
Not Found as a string
```

## Tip

Use `match` when you want a strict, expression-based choice. If no branch matches and you forget `default`, PHP throws an error instead of silently continuing.
