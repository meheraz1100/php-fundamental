# Include Once

`include_once` behaves like `include`, but PHP loads a particular file only once during the request. A missing file gives a warning and execution continues.

```php
<?php
include_once __DIR__ . '/helpers.php';
include_once __DIR__ . '/helpers.php';
echo 'Helpers requested twice.';
```

Expected output when the helper exists:

```text
Helpers requested twice.
```

The second include does not run the same file again, preventing duplicate function declarations.

Pitfall: `include_once` is not an error-handling strategy. Check that optional features can truly operate without the file.
