# PHP Fundamentals

PHP is an acronym for **PHP: Hypertext Preprocessor**. It is a widely used, open-source server-side scripting language for building dynamic websites and web applications. PHP scripts run on the server, and PHP is free to download and use.

## Basic Syntax

PHP code is written inside `<?php ... ?>` tags. The `echo` statement displays output:

```php
<?php
echo "Hello, World!";
?>
```

## Variables and Data Types

Variables begin with a dollar sign (`$`). PHP supports strings, integers, floats, booleans, arrays, and `null`.

```php
<?php
$name = "Rahim";
$age = 25;
$price = 99.50;
$isStudent = true;
?>
```

## Conditions

Use `if`, `elseif`, and `else` to make decisions:

```php
<?php
if ($age >= 18) {
    echo "You are an adult.";
} else {
    echo "You are underage.";
}
?>
```

## Loops

Loops repeat a block of code:

```php
<?php
for ($i = 1; $i <= 5; $i++) {
    echo $i . "<br>";
}
?>
```

## Arrays

Arrays store multiple values. They can use numeric indexes or named keys.

```php
<?php
$colors = ["Red", "Green", "Blue"];

$user = [
    "name" => "Rahim",
    "email" => "rahim@example.com"
];

echo $colors[0];       // Red
echo $user["name"];   // Rahim
?>
```

## Functions

Functions keep reusable code organized:

```php
<?php
function greet($name) {
    return "Hello, " . $name;
}

echo greet("Rahim");
?>
```

## Forms and Security

PHP can receive form data using `$_GET` and `$_POST`. Always validate user input and escape it before displaying it in HTML.

```php
<?php
$name = $_POST["name"] ?? "";
echo "Welcome, " . htmlspecialchars($name);
?>
```

## Database Access

PHP commonly connects to MySQL through PDO:

```php
<?php
$pdo = new PDO(
    "mysql:host=localhost;dbname=test",
    "root",
    ""
);
?>
```

These fundamentals are the foundation for building PHP websites, APIs, login systems, and database-driven applications.
