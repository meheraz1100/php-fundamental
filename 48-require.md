# Require

`require` inserts and runs another PHP file, but a missing file causes a fatal error and stops execution. Use it for essential configuration or shared code.

```php
<?php
require __DIR__ . '/config.php';
echo 'Application started';
```

If `config.php` exists, `Application started` is printed. If not, PHP stops with an error instead of running with missing configuration.

Tip: avoid building include paths directly from request input; attackers could otherwise attempt to load unintended files.
