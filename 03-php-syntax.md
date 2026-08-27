# PHP Syntax

PHP syntax is the set of rules that tells the interpreter how to read your code. A basic PHP file uses statements, semicolons, variables, and blocks wrapped in braces.

Most statements end with a semicolon. Whitespace and line breaks usually do not matter, but clear formatting makes code much easier to read and maintain.

## Example

```php
<?php
$name = "Amina";
$greeting = "Hello, " . $name;

echo $greeting . PHP_EOL;
echo 2 + 3;
```

## Expected Output

```text
Hello, Amina
5
```

## Tip

A missing semicolon is one of the most common syntax errors in PHP. When the parser fails, check the line before the error message too, because the real mistake is often just above the reported line.
