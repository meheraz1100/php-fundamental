# Registration

Registration creates an account after validating its input and hashing the password. This is an educational outline; production registration also needs HTTPS, CSRF protection, rate limiting, email verification, and duplicate-email handling.

```php
<?php
$email = filter_input(INPUT_POST, 'email', FILTER_VALIDATE_EMAIL);
$password = $_POST['password'] ?? '';
if (!$email || strlen($password) < 12) { exit('Use a valid email and 12+ character password.'); }
$hash = password_hash($password, PASSWORD_DEFAULT);
$statement = $pdo->prepare('INSERT INTO users (email, password_hash) VALUES (:email, :hash)');
$statement->execute(['email' => $email, 'hash' => $hash]);
echo 'Account created.';
```

With valid input and a unique email, the output is `Account created.`

Never store the raw password or log it. Enforce a database `UNIQUE` constraint on email and handle a duplicate-key error safely.

Tip: immediately send a verification flow rather than treating an unverified email address as fully trusted.
