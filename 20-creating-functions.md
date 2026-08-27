# Creating Functions

A function is a named block of reusable code. Define it once, then call it whenever that job is needed.

```php
<?php
function greet(): void
{
    echo "Hello, PHP!\n";
}

greet();
```

Expected output:

```text
Hello, PHP!
```

Function names are case-insensitive, but use one style consistently. Define functions before relying on them in code that is conditionally loaded.

Tip: give functions verb-like names such as `sendEmail` or `calculateTotal` so their purpose is clear.
