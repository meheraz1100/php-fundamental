# Password Hashing

Passwords must be stored as one-way hashes, not encrypted or plain text. PHP’s password API chooses a safe default algorithm and embeds the settings in the hash.

```php
<?php
$hash = password_hash('example-long-password', PASSWORD_DEFAULT);
echo password_verify('example-long-password', $hash) ? 'Verified' : 'Rejected';
```

Expected output:

```text
Verified
```

Store `$hash`, not the source password. On a successful login, use `password_needs_rehash()` to upgrade stored hashes if PHP’s recommended settings change.

Pitfall: never compare passwords or hashes with custom logic. Use `password_verify()`.
