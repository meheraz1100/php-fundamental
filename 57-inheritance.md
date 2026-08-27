# Inheritance

Inheritance lets a child class reuse and extend a parent class. Use it only for a genuine “is a” relationship.

```php
<?php
class Animal { public function sound(): string { return '...'; } }
class Dog extends Animal { public function sound(): string { return 'Woof'; } }
echo (new Dog())->sound();
```

Expected output:

```text
Woof
```

The child may override inherited methods while keeping the same promised behavior.

Pitfall: favor composition (one object containing another) when classes merely collaborate; inheritance can create tight coupling.
