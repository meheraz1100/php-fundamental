# Default Parameters

A default parameter value makes an argument optional. PHP uses the default when the caller leaves that argument out.

```php
<?php
function welcome(string $name, string $language = 'English'): void
{
    echo "Welcome, {$name}. Language: {$language}\n";
}

welcome('Nila');
welcome('Nila', 'Bangla');
```

Expected output:

```text
Welcome, Nila. Language: English
Welcome, Nila. Language: Bangla
```

The default belongs in the function declaration, not at every call site.

Pitfall: required parameters cannot follow optional parameters. Write `function example(string $required, string $optional = 'x')`.
