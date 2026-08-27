# Exception Handling

Exceptions signal exceptional failures. Catch expected exceptions to provide a controlled response, and use `finally` for cleanup that must always run.

```php
<?php
try {
    throw new RuntimeException('Connection failed');
} catch (RuntimeException $exception) {
    echo 'Please try again.';
} finally {
    echo ' Cleanup complete.';
}
```

Expected output:

```text
Please try again. Cleanup complete.
```

Log technical details on the server, but show users a safe generic message instead of database paths or secrets.

Pitfall: do not catch `Throwable` and silently ignore it; handle it meaningfully or let the application’s error handler log it.
