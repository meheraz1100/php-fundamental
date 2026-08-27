# PDO

PDO (PHP Data Objects) is PHP’s database abstraction API. Configure it to throw exceptions and use UTF-8 through the DSN.

```php
<?php
$pdo = new PDO(
    'mysql:host=127.0.0.1;dbname=school;charset=utf8mb4',
    getenv('DB_USER'),
    getenv('DB_PASSWORD'),
    [PDO::ATTR_ERRMODE => PDO::ERRMODE_EXCEPTION, PDO::ATTR_DEFAULT_FETCH_MODE => PDO::FETCH_ASSOC]
);
$count = $pdo->query('SELECT COUNT(*) FROM students')->fetchColumn();
echo "Students: {$count}";
```

With a populated table, the output has the form `Students: 24`.

This direct `query()` has no external values. Use `prepare()` and `execute()` whenever a value is dynamic.

Tip: catch `PDOException` at an application boundary, log it safely, and show users a generic error instead of connection details.
