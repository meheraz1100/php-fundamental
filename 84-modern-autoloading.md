# Modern Autoloading

PSR-4 autoloading maps a namespace prefix to a directory. Composer generates the loader, so PHP finds classes without manual `require` statements.

```json
{
  "autoload": {
    "psr-4": { "App\\": "src/" }
  }
}
```

```php
<?php
require __DIR__ . '/vendor/autoload.php';
$service = new App\Service\GreetingService();
echo $service->greet('Amina');
```

After `composer dump-autoload`, this outputs `Hello, Amina` when the matching class file exists.

Pitfall: namespace casing and directory/file names must match the PSR-4 mapping, especially on case-sensitive production servers.
