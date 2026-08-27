# POST

POST sends data in the request body. Use it for actions that create, update, or delete server state, and validate every submitted field.

```php
<?php
if ($_SERVER['REQUEST_METHOD'] !== 'POST') { exit('POST only'); }

$email = filter_input(INPUT_POST, 'email', FILTER_VALIDATE_EMAIL);
if ($email === false || $email === null) { http_response_code(422); exit('Valid email required'); }

echo 'Saved: ' . htmlspecialchars($email, ENT_QUOTES, 'UTF-8');
```

Posting `email=person@example.com` displays `Saved: person@example.com`.

Pitfall: POST does not encrypt data. Use HTTPS, and protect state-changing forms with CSRF tokens in production.
