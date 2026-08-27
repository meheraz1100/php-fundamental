# Constructors

A constructor is the `__construct` method PHP runs when an object is created. It establishes valid initial state.

```php
<?php
class User
{
    public function __construct(public string $name) {}
}
$user = new User('Rafi');
echo $user->name;
```

Expected output:

```text
Rafi
```

`public string $name` in a constructor parameter is property promotion: it declares and assigns the property in one place.

Tip: validate constructor arguments when invalid values would create an unusable object.
