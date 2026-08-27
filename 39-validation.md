# Validation

Validation checks whether input is acceptable for your application: required, correctly shaped, and within sensible limits. Do it on the server before saving or acting on data.

```php
<?php
$age = filter_input(INPUT_POST, 'age', FILTER_VALIDATE_INT, ['options' => ['min_range' => 13, 'max_range' => 120]]);
if ($age === false || $age === null) { http_response_code(422); exit('Age must be 13 to 120.'); }
echo "Accepted age: {$age}";
```

Posting `age=20` displays `Accepted age: 20`.

Tip: use allow-lists for known choices (for example, roles) rather than trying to block every bad value.
