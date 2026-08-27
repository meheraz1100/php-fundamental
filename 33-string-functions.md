# String Functions

Strings are sequences of characters. PHP has functions for measuring, trimming, searching, and changing text.

```php
<?php
$message = '  Learn PHP  ';
$clean = trim($message);

echo strlen($clean) . PHP_EOL;
echo strtolower($clean) . PHP_EOL;
```

Expected output:

```text
9
learn php
```

Other useful functions are `str_contains`, `str_replace`, `substr`, and `strtoupper`.

Pitfall: `strlen()` counts bytes. For user-facing UTF-8 text such as Bangla, use `mb_strlen()` when the mbstring extension is available.
