# CRUD

CRUD means Create, Read, Update, and Delete. Use prepared PDO statements for each operation when values come from a request or user.

```php
<?php
$pdo = new PDO($dsn, $user, $password, [PDO::ATTR_ERRMODE => PDO::ERRMODE_EXCEPTION]);
$statement = $pdo->prepare('UPDATE students SET name = :name WHERE id = :id');
$statement->execute(['name' => 'Amina', 'id' => 7]);
echo $statement->rowCount() . ' row updated';
```

If row `7` changes, output is `1 row updated`.

Create uses `INSERT`, read uses `SELECT`, update uses `UPDATE`, and delete uses `DELETE`.

Pitfall: validate the ID and authorization before changes; parameter binding prevents injection but does not decide who is allowed to edit a record.
