# Multidimensional Arrays

A multidimensional array contains other arrays. It can represent rows of related data without creating objects.

```php
<?php
$students = [
    ['name' => 'Mina', 'score' => 92],
    ['name' => 'Tariq', 'score' => 88],
];

echo $students[1]['name'] . ': ' . $students[1]['score'] . PHP_EOL;
```

Expected output:

```text
Tariq: 88
```

Read nested data one level at a time: array index first, then the inner key.

Pitfall: deeply nested arrays become difficult to maintain. Consider a class or separate data structure when the shape grows complex.
