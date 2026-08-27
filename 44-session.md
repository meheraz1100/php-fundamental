# SESSION

`$_SESSION` stores data across requests for one browser session. Call `session_start()` before output and regenerate the ID after authentication.

```php
<?php
session_set_cookie_params(['httponly' => true, 'secure' => true, 'samesite' => 'Lax']);
session_start();
$_SESSION['flash'] = 'Settings saved.';
echo $_SESSION['flash'];
```

Expected output:

```text
Settings saved.
```

For local HTTP development, omit `secure => true`; production sites should use HTTPS.

Tip: store a user ID and retrieve current permissions server-side, rather than storing trusted roles from the browser.
