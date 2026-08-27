# Sessions

Sessions associate server-side data with a browser cookie. Configure the cookie before `session_start()` and regenerate the session ID immediately after login.

```php
<?php
session_set_cookie_params(['httponly' => true, 'secure' => true, 'samesite' => 'Lax']);
session_start();
session_regenerate_id(true);
$_SESSION['user_id'] = 42;
echo 'Authenticated session created.';
```

Expected output:

```text
Authenticated session created.
```

Use HTTPS in production for the `Secure` flag; local HTTP development may need it disabled. Set session timeouts and destroy sessions on logout.

Tip: a session proves authentication, not authorization. Re-check permissions before sensitive actions.
