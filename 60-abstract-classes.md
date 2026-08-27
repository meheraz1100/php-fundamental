# Abstract Classes

An abstract class is a partial blueprint that cannot be instantiated itself. It can share implementation while requiring children to supply specific methods.

```php
<?php
abstract class Shape { abstract public function area(): float; }
class Square extends Shape { public function __construct(private float $side) {} public function area(): float { return $this->side ** 2; } }
echo (new Square(4))->area();
```

Expected output:

```text
16
```

Abstract classes may contain normal properties and methods in addition to abstract methods.

Pitfall: PHP supports only one parent class, so use interfaces or composition when behavior must cross several unrelated types.
