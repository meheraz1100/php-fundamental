# Writing Files

`file_put_contents` writes a string to a file. Use a fixed application directory, handle write failures, and use `LOCK_EX` when concurrent writes may occur.

```php
<?php
$path = __DIR__ . '/data/message.txt';
$bytes = file_put_contents($path, "Saved safely\n", LOCK_EX);
if ($bytes === false) { throw new RuntimeException('Could not write message.'); }
echo "Wrote {$bytes} bytes.";
```

Expected output:

```text
Wrote 13 bytes.
```

Ensure the `data` directory is writable by PHP and is not a place where uploaded executable files can run.

Pitfall: never let user input choose the target path; this can overwrite sensitive files.
