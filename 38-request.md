# REQUEST

`$_REQUEST` combines values from GET, POST, and often cookies. It can be convenient for a quick experiment, but it hides where input came from.

```php
<?php
$page = $_REQUEST['page'] ?? 'home';
echo htmlspecialchars((string) $page, ENT_QUOTES, 'UTF-8');
```

For `?page=about`, the output is `about`.

Prefer `$_GET` or `$_POST` when the source matters; a cookie or query parameter can unexpectedly override a POST value depending on server configuration.

Tip: cast and validate the value even after selecting a superglobal.
