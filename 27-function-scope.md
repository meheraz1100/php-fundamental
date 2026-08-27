# Function Scope

Variables created inside a function are local to that function. A function can access global state only when you deliberately pass it in, use `global`, or read `$GLOBALS`; passing values is usually clearer.

```php
<?php
function nextVisit(): int
{
    static $visits = 0;
    $visits++;
    return $visits;
}

echo nextVisit() . PHP_EOL;
echo nextVisit() . PHP_EOL;
```

Expected output:

```text
1
2
```

`static $visits` keeps its value between calls while still being local to `nextVisit`.

Pitfall: avoid using `global` for ordinary dependencies; it hides what a function needs and makes testing harder.
