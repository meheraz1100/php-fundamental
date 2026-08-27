# HTML Forms with PHP

An HTML form sends named fields to a PHP script. Use `method="post"` for changes such as creating data, and escape any submitted value before placing it in HTML.

```php
<!-- form.html -->
<form method="post" action="handle.php">
  <label>Name <input name="name" required></label>
  <button>Send</button>
</form>
```

```php
<?php // handle.php
$name = trim($_POST['name'] ?? '');
if ($name === '') { http_response_code(422); exit('Name is required.'); }
echo 'Hello, ' . htmlspecialchars($name, ENT_QUOTES, 'UTF-8');
```

Submit `Amina` to see `Hello, Amina`.

Pitfall: `required` is only a browser convenience. Always validate again in PHP.
