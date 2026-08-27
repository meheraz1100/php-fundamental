# Autoloading

Autoloading loads a class file only when PHP first needs that class. Composer provides the standard, reliable autoloader for modern projects.

```php
<?php
require __DIR__ . '/vendor/autoload.php';

use App\Greeter;
echo (new Greeter())->message();
```

With Composer PSR-4 mapping `App\\` to `src/`, PHP loads `src/Greeter.php` automatically and prints that method's result.

Tip: run `composer dump-autoload` after changing `composer.json` autoload rules; do not manually require every class file.
