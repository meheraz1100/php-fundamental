# GET Superglobal

`$_GET` is an associative array of query-string parameters. A URL such as `profile.php?id=12` creates `$_GET['id']`.

```php
<?php
$id = filter_input(INPUT_GET, 'id', FILTER_VALIDATE_INT, ['options' => ['min_range' => 1]]);
if ($id === false || $id === null) { exit('A positive id is required.'); }
echo "Profile id: {$id}";
```

Visiting `profile.php?id=12` outputs `Profile id: 12`.

Tip: a query parameter is always untrusted input, even if your own page generated the link.
