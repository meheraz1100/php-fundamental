# JSON Handling

JSON exchanges structured data as text. Use `json_encode` to create JSON and `json_decode` with exceptions to detect invalid JSON clearly.

```php
<?php
try {
    $json = json_encode(['name' => 'Amina', 'active' => true], JSON_THROW_ON_ERROR);
    $data = json_decode($json, true, 512, JSON_THROW_ON_ERROR);
    echo $data['name'];
} catch (JsonException $exception) {
    http_response_code(400);
    echo 'Invalid JSON.';
}
```

Expected output:

```text
Amina
```

The `true` argument makes `json_decode` return associative arrays rather than objects.

Tip: validate decoded fields and types before using them; valid JSON is not automatically valid application data.
