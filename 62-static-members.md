# Static Members

Static properties and methods belong to the class itself rather than a particular object. Access them with `::`.

```php
<?php
class MathTools
{
    public static function double(int $number): int { return $number * 2; }
}
echo MathTools::double(8);
```

Expected output:

```text
16
```

Static methods do not have `$this`, so they cannot read instance state unless an object is passed in.

Pitfall: avoid using static state as a hidden global store; it can make tests and request behavior harder to reason about.
