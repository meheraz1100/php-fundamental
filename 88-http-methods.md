# HTTP Methods

HTTP methods communicate the intended operation. Use them consistently so clients, caches, and security controls can understand an endpoint.

```php
<?php
$method = $_SERVER['REQUEST_METHOD'] ?? 'GET';
if ($method === 'GET') { echo 'Read resource'; }
elseif ($method === 'POST') { http_response_code(201); echo 'Created resource'; }
else { http_response_code(405); echo 'Method not allowed'; }
```

A GET request outputs `Read resource`; a POST request returns status 201 and `Created resource`.

Typical choices: GET reads, POST creates/actions, PUT replaces, PATCH partially updates, and DELETE removes. Use status codes such as 200, 201, 204, 400, 401, 403, 404, and 422 accurately.

Pitfall: never use GET for a destructive action; links, prefetchers, and caches may trigger it.
