# Authorization

Authorization decides whether an authenticated user may perform a particular action. Check the server-side user ID and role before changing protected data.

```php
<?php
session_start();
if (($_SESSION['role'] ?? null) !== 'admin') {
    http_response_code(403);
    exit('Forbidden');
}
echo 'Admin area';
```

For a session role of `admin`, output is `Admin area`; other users receive a 403 response.

In a production app, load current roles and ownership from the database or trusted authorization service rather than trusting a client value.

Pitfall: hiding a button is not authorization. Enforce checks in every server endpoint that performs a privileged action.
