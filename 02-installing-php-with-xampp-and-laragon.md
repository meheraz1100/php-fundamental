# Installing PHP With XAMPP and Laragon

XAMPP and Laragon are popular local development stacks that bundle PHP with a web server and database tools. They make it easy to run PHP files on your computer without deploying to a live host.

With XAMPP, you usually place files in `htdocs`. With Laragon, you usually work inside the `www` folder. In both cases, the server handles PHP for you when you visit the file through `http://localhost/...`.

## Example

```php
<?php
echo "PHP version: " . PHP_VERSION . PHP_EOL;
echo "Server API: " . PHP_SAPI . PHP_EOL;
echo "Document root example: put this file in htdocs or www." . PHP_EOL;
```

## Expected Output

```text
PHP version: 8.x.x
Server API: cli
Document root example: put this file in htdocs or www.
```

If you open the file through a browser on XAMPP or Laragon, the first two lines still confirm that PHP is installed and working, but the server API may differ.

## Tip

After installation, verify the setup with `php -v` in a terminal and by loading a simple `.php` file in the browser. If both work, your environment is ready.
