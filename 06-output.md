# Output

Output is how PHP sends data back to the user. The most common tools are `echo`, `print`, and `printf`. They can write plain text, HTML, or formatted values.

`echo` is the most common choice for simple output. `printf` is useful when you want control over formatting, such as numbers or dates.

## Example

```php
<?php
$name = "Nadia";
$score = 92.5;

echo "Hello, " . $name . PHP_EOL;
print "Your score is " . $score . PHP_EOL;
printf("Rounded score: %.0f" . PHP_EOL, $score);
```

## Expected Output

```text
Hello, Nadia
Your score is 92.5
Rounded score: 93
```

## Tip

When outputting user data into HTML, escape it with `htmlspecialchars()` first. That helps prevent broken markup and cross-site scripting issues.
