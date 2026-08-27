# Explode and Implode

`explode()` splits a string into an array using a separator. `implode()` joins array values into one string.

```php
<?php
$tags = explode(',', 'php,html,mysql');
echo $tags[1] . PHP_EOL;
echo implode(' | ', $tags) . PHP_EOL;
```

Expected output:

```text
html
php | html | mysql
```

Use a delimiter that cannot be confused with the data, or trim values after splitting user input.

Tip: `implode(', ', array_map('trim', $tags))` can produce a clean display list after splitting text with spaces.
