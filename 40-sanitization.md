# Sanitization

Sanitization transforms input; validation decides whether it is allowed. The safest HTML output practice is context-aware escaping with `htmlspecialchars`.

```php
<?php
$raw = '<script>alert(1)</script> Amina';
$safeForHtml = htmlspecialchars($raw, ENT_QUOTES | ENT_SUBSTITUTE, 'UTF-8');
echo $safeForHtml;
```

Expected browser text:

```text
<script>alert(1)</script> Amina
```

The script is displayed as text instead of executing.

Pitfall: escaping for HTML is not a substitute for SQL parameter binding, URL encoding, or JavaScript-string escaping; each output context needs its own handling.
