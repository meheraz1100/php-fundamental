# COOKIE

Cookies are small browser-stored values sent with future requests. Set them before output; read them through `$_COOKIE` on a later request.

```php
<?php
setcookie('theme', 'dark', ['expires' => time() + 86400, 'httponly' => true, 'secure' => true, 'samesite' => 'Lax']);
echo 'Theme cookie scheduled.';
```

Expected output:

```text
Theme cookie scheduled.
```

The cookie becomes available in `$_COOKIE['theme']` on the next request.

Pitfall: cookies are user-controlled. Never store passwords, secrets, or authorization decisions in them; use `Secure` only over HTTPS.
