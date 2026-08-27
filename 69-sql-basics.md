# SQL Basics

SQL queries select, filter, sort, and change relational data. Keep SQL keywords readable and bind all values that originate outside your code.

```php
<?php
$statement = $pdo->prepare('SELECT id, name FROM students WHERE score >= :minimum ORDER BY name ASC');
$statement->execute(['minimum' => 80]);
$rows = $statement->fetchAll(PDO::FETCH_ASSOC);
print_r($rows);
```

For matching rows, `print_r` displays an array containing each selected `id` and `name`.

`SELECT`, `INSERT`, `UPDATE`, and `DELETE` are core SQL commands; `WHERE` narrows rows and `ORDER BY` controls ordering.

Tip: placeholders bind values, not SQL identifiers. Choose table and column names from trusted application code.
