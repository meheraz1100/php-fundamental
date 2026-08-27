# Packages

A package is reusable PHP code published through a registry such as Packagist or maintained in a private repository. Composer resolves its version constraints and dependencies.

```json
{
  "require": {
    "monolog/monolog": "^3.0"
  }
}
```

Run `composer update monolog/monolog` to select an allowed newer version and update the lock file.

`^3.0` allows compatible 3.x releases but not 4.0. Read a package’s documentation, license, maintenance status, and security advisories before adding it.

Pitfall: avoid an unrestricted `*` constraint. Locking dependencies helps make development and production use the same code.
