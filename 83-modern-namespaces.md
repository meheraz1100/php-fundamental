# Modern Namespaces

In modern applications, namespaces mirror an application’s logical areas and prevent collisions with packages. Composer maps namespace prefixes to directories.

```php
<?php
namespace App\Service;

class GreetingService
{
    public function greet(string $name): string { return "Hello, {$name}"; }
}
```

With a PSR-4 `App\\` mapping to `src/`, save this class as `src/Service/GreetingService.php` and import it with `use App\Service\GreetingService;`.

Tip: organize namespaces around the application, not a vendor’s internals; keep one clear class per file for predictable autoloading.
