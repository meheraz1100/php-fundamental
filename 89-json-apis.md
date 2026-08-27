# JSON APIs

A JSON API should declare its response type, encode data safely, and use clear error status codes. Validate JSON request bodies before using them.

```php
<?php
header('Content-Type: application/json; charset=utf-8');
try {
    $input = json_decode(file_get_contents('php://input'), true, 512, JSON_THROW_ON_ERROR);
    if (!is_string($input['name'] ?? null) || trim($input['name']) === '') { throw new InvalidArgumentException(); }
    http_response_code(201);
    echo json_encode(['name' => trim($input['name'])], JSON_THROW_ON_ERROR);
} catch (JsonException|InvalidArgumentException) {
    http_response_code(422); echo json_encode(['error' => 'Invalid request']);
}
```

Posting `{"name":"Amina"}` returns status 201 and `{"name":"Amina"}`. Invalid JSON or a missing name returns status 422 with a generic error.

Tip: use HTTPS, authentication, authorization, request-size limits, and rate limits in production; do not leak stack traces or secrets in JSON errors.
