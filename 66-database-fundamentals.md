# Database Fundamentals

A relational database stores data in tables made of rows and columns. MySQL is a common database server; PHP connects to it through PDO.

```php
<?php
$pdo = new PDO('mysql:host=127.0.0.1;dbname=school;charset=utf8mb4', getenv('DB_USER'), getenv('DB_PASSWORD'), [
    PDO::ATTR_ERRMODE => PDO::ERRMODE_EXCEPTION,
]);
echo 'Connected';
```

With valid local credentials and a `school` database, the output is `Connected`.

Keep credentials in deployment environment variables, not source code.

Tip: use a least-privilege database account instead of a root account for web applications.
