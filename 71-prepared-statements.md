# Prepared Statements

A prepared statement keeps SQL structure separate from values. It is the standard defense against SQL injection for database values.

```php
<?php
$email = filter_input(INPUT_POST, 'email', FILTER_VALIDATE_EMAIL);
if (!$email) { exit('Valid email required'); }
$statement = $pdo->prepare('SELECT id, name FROM students WHERE email = :email');
$statement->execute(['email' => $email]);
$student = $statement->fetch(PDO::FETCH_ASSOC);
var_dump($student);
```

The output is either an associative student array or `bool(false)` when no row matches.

Named placeholders make queries easy to read; positional `?` placeholders also work.

Pitfall: never concatenate user input into SQL, even after escaping. Use a placeholder for every user-supplied value.
