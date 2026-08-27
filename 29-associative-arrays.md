# Associative Arrays

An associative array maps meaningful string keys to values. It is useful for a record such as a user profile.

```php
<?php
$user = [
    'name' => 'Asha',
    'city' => 'Dhaka',
];

echo $user['name'] . ' lives in ' . $user['city'] . PHP_EOL;
```

Expected output:

```text
Asha lives in Dhaka
```

Keys are case-sensitive: `'name'` and `'Name'` are different keys.

Tip: use `??` for a safe fallback, such as `$name = $user['name'] ?? 'Guest';`.
