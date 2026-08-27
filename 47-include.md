# Include

`include` inserts and runs another PHP file. If the file is missing, PHP emits a warning and continues execution.

```php
<?php
// header.php contains: <h1>My site</h1>
include __DIR__ . '/header.php';
echo 'Content';
```

When `header.php` exists, the page shows its heading followed by `Content`.

Use `__DIR__` to build a stable path relative to the current file.

Pitfall: continuing after a missing include can leave a page incomplete; use `require` when the dependency is essential.
