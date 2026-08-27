# MVC Architecture

MVC separates an application into Models (data and rules), Views (presentation), and Controllers (request coordination). This makes each responsibility easier to change and test.

```php
<?php
// Controller idea: get a model result, then choose a view.
$user = ['name' => 'Amina']; // normally from a model/repository
require __DIR__ . '/views/profile.php';
```

If `views/profile.php` safely echoes `$user['name']`, the rendered page shows Amina’s profile.

The controller should validate input and choose the response; the view should escape display data; the model should not depend on HTML.

Tip: MVC is a boundary guide, not a reason to put all logic into a giant controller.
