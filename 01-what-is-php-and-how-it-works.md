# What Is PHP and How It Works

PHP is a server-side scripting language. That means the code runs on the web server first, then sends HTML, JSON, or other output to the browser. The browser never sees the PHP source itself.

When a request arrives, the server hands the `.php` file to the PHP runtime. PHP executes the code from top to bottom, talks to databases or files if needed, and returns a response. That response is what the browser renders.

## Example

```php
<?php
echo "PHP runs on the server." . PHP_EOL;
echo "Runtime: " . PHP_VERSION . PHP_EOL;
echo "Interface: " . PHP_SAPI . PHP_EOL;
```

## Expected Output

```text
PHP runs on the server.
Runtime: 8.x.x
Interface: cli
```

If you run the same file through a web server, `PHP_SAPI` will usually show a web value such as `apache2handler` or `fpm-fcgi` instead of `cli`.

## Tip

PHP code only runs inside PHP tags. Anything outside them is sent as plain text, which is useful when mixing HTML with dynamic content.
