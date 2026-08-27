# File Uploads

Uploads arrive in `$_FILES`. Accept them only after checking the upload error, a size limit, and the detected file content type; generate your own storage name.

```php
<?php
$file = $_FILES['photo'] ?? null;
if (!$file || $file['error'] !== UPLOAD_ERR_OK || $file['size'] > 2_000_000) { exit('Invalid upload.'); }
$mime = (new finfo(FILEINFO_MIME_TYPE))->file($file['tmp_name']);
if (!in_array($mime, ['image/jpeg', 'image/png'], true)) { exit('JPEG or PNG only.'); }
$destination = __DIR__ . '/uploads/' . bin2hex(random_bytes(16)) . ($mime === 'image/png' ? '.png' : '.jpg');
if (!move_uploaded_file($file['tmp_name'], $destination)) { exit('Could not store upload.'); }
echo 'Uploaded.';
```

Use it with a `multipart/form-data` form and an input named `photo`; a successful upload prints `Uploaded.`

Pitfall: never trust the original filename or browser-declared MIME type. Store uploads outside the web root where possible and prevent executable uploads.
