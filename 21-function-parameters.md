# Function Parameters

Parameters are values a function receives from its caller. They let one function work with different input.

```php
<?php
function greetPerson(string $name): void
{
    echo "Hello, {$name}!\n";
}

greetPerson('Amina');
greetPerson('Rafi');
```

Expected output:

```text
Hello, Amina!
Hello, Rafi!
```

`$name` is a parameter; `'Amina'` is an argument. Parameters are passed by value by default, so changing one inside the function does not change the caller's variable.

Pitfall: parameter order matters. Put required parameters before optional ones.
