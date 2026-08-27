# ENV

`$_ENV` may contain environment variables supplied by the server or process. It is suitable for configuration, but availability depends on PHP/server settings.

```php
<?php
$environment = $_ENV['APP_ENV'] ?? getenv('APP_ENV') ?: 'production';
echo "Environment: {$environment}";
```

With `APP_ENV=development`, the output is `Environment: development`.

Tip: keep real secrets in the deployment environment or an uncommitted local configuration file. Never print values such as database passwords or API keys.
