# PSR Standards

PHP-FIG PSRs are interoperability recommendations. They help packages and applications use familiar interfaces, autoloading, and coding conventions.

```php
<?php
// PSR-12-style formatting: braces on their own line and four-space indentation.
function formatName(string $name): string
{
    return trim($name);
}

echo formatName(' Amina ');
```

Expected output:

```text
Amina
```

Common standards include PSR-4 for autoloading, PSR-3 for logging interfaces, PSR-7 for HTTP messages, and PSR-12 for coding style.

Tip: a standard is useful when your project and its dependencies agree to it; check what your chosen framework actually supports.
