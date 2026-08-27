# Environment Files

Environment variables separate configuration from code. A local `.env` file is often loaded during development, while production platforms usually supply variables directly.

```dotenv
APP_ENV=development
DB_HOST=127.0.0.1
DB_NAME=school
```

```php
<?php
echo getenv('APP_ENV') ?: 'production';
```

When `APP_ENV=development` is available, output is `development`.

Never commit real passwords, API keys, tokens, or private URLs to `.env`; add `.env` to `.gitignore` and commit a secret-free `.env.example` only when helpful.
