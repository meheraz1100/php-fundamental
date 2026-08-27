# Traits

A trait shares method implementations across unrelated classes. Import it with `use` inside each class that needs the behavior.

```php
<?php
trait Timestamped { public function createdLabel(): string { return 'Created now'; } }
class Post { use Timestamped; }
echo (new Post())->createdLabel();
```

Expected output:

```text
Created now
```

Traits reduce duplication, but they are copied into the class rather than becoming a separate object.

Tip: keep traits small and focused; use composition for stateful services with dependencies.
