# Classes and Objects

A class is a blueprint; an object is one value created from that blueprint. Classes group data and behavior that belong together.

```php
<?php
class Book
{
    public string $title;
}

$book = new Book();
$book->title = 'PHP Basics';
echo $book->title;
```

Expected output:

```text
PHP Basics
```

`new Book()` creates an object and `->` accesses an object member.

Tip: prefer methods and private properties for important invariants instead of exposing all data publicly.
