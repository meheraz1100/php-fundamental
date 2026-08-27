# Properties and Methods

Properties hold an object's state; methods are functions declared inside a class that operate on that state.

```php
<?php
class Counter
{
    public int $value = 0;
    public function increment(): void { $this->value++; }
}
$counter = new Counter();
$counter->increment();
echo $counter->value;
```

Expected output:

```text
1
```

Inside an instance method, `$this` refers to the current object.

Pitfall: typed properties must be initialized before reading them, unless they are declared nullable with a default of `null`.
