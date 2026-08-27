# Interfaces

An interface defines methods a class promises to provide. It describes a capability without choosing its implementation.

```php
<?php
interface Notifier { public function send(string $message): void; }
class ConsoleNotifier implements Notifier { public function send(string $message): void { echo $message; } }
(new ConsoleNotifier())->send('Done');
```

Expected output:

```text
Done
```

A class can implement multiple interfaces, making it useful where code depends on a shared contract.

Tip: type-hint against an interface when callers need behavior, not a particular concrete class.
