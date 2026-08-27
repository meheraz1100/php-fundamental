# Encapsulation

Encapsulation hides an object's internal state and exposes controlled operations. Use `private` properties to stop outside code from breaking rules.

```php
<?php
class BankAccount
{
    private int $balance = 0;
    public function deposit(int $amount): void { if ($amount > 0) { $this->balance += $amount; } }
    public function balance(): int { return $this->balance; }
}
$account = new BankAccount(); $account->deposit(500); echo $account->balance();
```

Expected output:

```text
500
```

`private` members are accessible only inside their declaring class.

Tip: expose the smallest useful public API; this makes later changes safer.
