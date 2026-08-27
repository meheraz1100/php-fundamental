# Namespaces

Namespaces prevent class-name collisions by grouping names. Declare the namespace at the top of a PHP class file, then import it where used.

```php
<?php
namespace App;
class Greeter { public function message(): string { return 'Hello'; } }

$greeter = new Greeter();
echo $greeter->message();
```

Expected output:

```text
Hello
```

In another namespace, refer to this class as `\App\Greeter` or import it with `use App\Greeter;`.

Tip: one namespace declaration must be the first statement after `<?php` (apart from `declare`).
