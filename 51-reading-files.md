# Reading Files

Read only known, server-controlled paths. Check failures so a missing or unreadable file does not turn into misleading application output.

```php
<?php
$path = __DIR__ . '/notes.txt';
$contents = @file_get_contents($path);
if ($contents === false) { throw new RuntimeException('Could not read notes.'); }
echo $contents;
```

If `notes.txt` contains `Study PHP`, the output is:

```text
Study PHP
```

Tip: do not pass a filename from `$_GET` directly to file functions. Map allowed names to fixed paths instead.
