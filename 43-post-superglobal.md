# POST Superglobal

`$_POST` contains fields submitted in a POST request, usually from an HTML form. It is empty on GET requests.

```php
<?php
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $message = trim((string) ($_POST['message'] ?? ''));
    echo htmlspecialchars($message, ENT_QUOTES, 'UTF-8');
}
```

Posting `message=Hello` outputs `Hello`.

Pitfall: do not assume a form field exists or has the expected type; use a fallback, validate it, and escape it when rendering.
