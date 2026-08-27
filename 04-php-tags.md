# PHP Tags

PHP tags tell the server where PHP code starts and ends. The standard open tag is `<?php`, and the closing tag is `?>`. In pure PHP files, the closing tag is often omitted to avoid accidental whitespace output.

PHP code can also be mixed with HTML. That is one of the reasons PHP is so common for dynamic web pages.

## Example

```php
<?php
$title = "Welcome";
?>
<h1><?php echo $title; ?></h1>
<p>This HTML is mixed with PHP.</p>
```

## Expected Output

```html
<h1>Welcome</h1>
<p>This HTML is mixed with PHP.</p>
```

## Tip

Use `<?php` instead of short tags like `<?`. Short tags are not reliable across all server configurations, while `<?php` always works.
