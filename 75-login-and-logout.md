# Login and Logout

Login verifies a submitted password against the stored hash, then starts an authenticated session. Logout clears the session and its cookie.

```php
<?php
session_start();
$email = filter_input(INPUT_POST, 'email', FILTER_VALIDATE_EMAIL);
if (!$email) { http_response_code(401); exit('Invalid credentials.'); }
$statement = $pdo->prepare('SELECT id, password_hash FROM users WHERE email = :email');
$statement->execute(['email' => $email]);
$user = $statement->fetch(PDO::FETCH_ASSOC);
if ($user && password_verify((string) ($_POST['password'] ?? ''), $user['password_hash'])) {
    session_regenerate_id(true); $_SESSION['user_id'] = $user['id']; echo 'Logged in.';
} else { http_response_code(401); echo 'Invalid credentials.'; }
```

Successful credentials output `Logged in.` A logout handler can call `$_SESSION = []; session_destroy();` and expire the session cookie.

Pitfall: return the same generic failure for unknown emails and wrong passwords, and rate-limit attempts in production to reduce account enumeration and brute force.
