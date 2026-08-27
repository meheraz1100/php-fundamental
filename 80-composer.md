# Composer

Composer is PHP’s dependency manager. It records required packages in `composer.json`, installs them into `vendor/`, and creates `vendor/autoload.php`.

```powershell
composer init
composer require monolog/monolog
composer install
```

`composer require` updates `composer.json` and `composer.lock`; `composer install` installs the exact locked versions.

Use installed packages in PHP with `require __DIR__ . '/vendor/autoload.php';`.

Tip: commit `composer.json` and `composer.lock`, but do not commit `vendor/` for most applications unless a deployment policy explicitly requires it.
