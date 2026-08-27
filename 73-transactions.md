# Transactions

A transaction groups database changes so they all succeed together or all roll back. Use one for operations such as transferring money or creating several related records.

```php
<?php
$pdo->beginTransaction();
try {
    $pdo->prepare('UPDATE accounts SET balance = balance - :amount WHERE id = :id')->execute(['amount' => 50, 'id' => 1]);
    $pdo->prepare('UPDATE accounts SET balance = balance + :amount WHERE id = :id')->execute(['amount' => 50, 'id' => 2]);
    $pdo->commit();
    echo 'Transfer complete';
} catch (Throwable $exception) {
    if ($pdo->inTransaction()) { $pdo->rollBack(); }
    throw $exception;
}
```

When both updates succeed, the output is `Transfer complete`; otherwise the changes are rolled back.

Pitfall: validate amounts and authorize both accounts before starting. A transaction preserves consistency but does not supply business rules.
