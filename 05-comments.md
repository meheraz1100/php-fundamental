# Comments

Comments are notes for humans. PHP ignores them when running the program. Use comments to explain why something exists, not to repeat what obvious code already says.

PHP supports single-line comments with `//` and `#`, and multi-line comments with `/* ... */`.

## Example

```php
<?php
// This is a single-line comment.
# This also works.
/*
   This is a multi-line comment.
*/

echo "Comments do not appear in output." . PHP_EOL;
```

## Expected Output

```text
Comments do not appear in output.
```

## Tip

Comments can become stale. If a comment no longer matches the code, update or remove it so it does not mislead the next person reading the file.
