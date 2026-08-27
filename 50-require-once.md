# Require Once

`require_once` loads an essential file one time per request. It stops execution if the file cannot be found and avoids duplicate class or function declarations.

```php
<?php
require_once __DIR__ . '/bootstrap.php';
require_once __DIR__ . '/bootstrap.php';
echo 'Bootstrapped once.';
```

Expected output when `bootstrap.php` exists:

```text
Bootstrapped once.
```

Use this for application bootstrap files and hand-written class dependencies. Composer autoloading is the usual modern alternative for classes.

Tip: choose `require_once` when a missing dependency would make the rest of the request unsafe or meaningless.
