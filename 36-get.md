# GET

GET sends form data in the URL query string. It is appropriate for safe, bookmarkable actions such as search, not passwords or data changes.

```php
<!-- search.html -->
<form method="get" action="search.php"><input name="q"><button>Search</button></form>
```

```php
<?php // search.php?q=php
$query = trim($_GET['q'] ?? '');
echo 'Searching for: ' . htmlspecialchars($query, ENT_QUOTES, 'UTF-8');
```

Visiting `search.php?q=php` displays `Searching for: php`.

Tip: validate length and allowed characters before using a query in business logic or a database query.
