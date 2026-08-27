# Basic Security Practices

Security is a set of layers: validate input, escape output, bind database values, hash passwords, protect sessions, and authorize every sensitive action.

```php
<?php
$name = trim((string) ($_POST['name'] ?? ''));
if ($name === '' || strlen($name) > 100) { exit('Invalid name'); }
echo htmlspecialchars($name, ENT_QUOTES | ENT_SUBSTITUTE, 'UTF-8');
```

Posting `Amina` displays `Amina`; HTML-like input is rendered as text.

Production essentials include HTTPS, CSRF tokens for state-changing browser requests, rate limits, security updates, error logging without secrets, and least-privilege accounts.

Tip: prepared statements prevent SQL injection but do not replace validation, output escaping, access control, or a security review.
