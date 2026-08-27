# PHP Fundamentals Lessons Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a complete, standalone Markdown lesson for every PHP topic requested by the user.

**Architecture:** Keep lessons flat at the repository root, with ordered `NN-topic-name.md` filenames. Each file teaches exactly one topic using a concise explanation, PHP 8+ examples, expected usage/output, and safety notes where relevant. The root README is a link-only course index.

**Tech Stack:** Markdown, PHP 8+, HTML form snippets, MySQL/PDO examples, Composer concepts.

**Spec:** `docs/superpowers/specs/2026-08-27-php-fundamentals-lessons-design.md`

## Global Constraints

- Create exactly one Markdown file for every user-listed topic.
- Use unique, sequential numeric filenames at the repository root.
- Keep each lesson self-contained; do not depend on another lesson for required explanation.
- Use PDO prepared statements for database examples.
- Teach validation, escaping, password hashing, and session security in applicable lessons.
- Use balanced Markdown fences and valid PHP 8+ syntax.

---

### Task 1: Fundamentals lessons

**Files:** Create `01-what-is-php-and-how-it-works.md` through `11-operators.md`.

- [ ] Write eleven files covering PHP lifecycle, installation with XAMPP/Laragon, syntax, PHP tags, comments, output, variables, constants, data types, casting, and operators.
- [ ] Include one runnable example and an expected result in every file.
- [ ] Verify filenames and code fences: `rg -l '^# ' 0*.md 1[01]-*.md`.
- [ ] Commit: `git add 0*.md 10-*.md 11-*.md && git commit -m "Add PHP fundamentals lessons"`.

### Task 2: Control flow lessons

**Files:** Create `12-if-else-elseif.md`, `13-switch.md`, `14-match.md`, `15-for-loop.md`, `16-while-loop.md`, `17-do-while-loop.md`, `18-foreach.md`, `19-break-and-continue.md`.

- [ ] Explain branching and iteration, including strict matching for `match` and loop-control effects.
- [ ] Include executable code and expected output in every file.
- [ ] Verify eight lesson headings: `rg -l '^# ' 12-*.md 13-*.md 14-*.md 15-*.md 16-*.md 17-*.md 18-*.md 19-*.md`.
- [ ] Commit: `git add 12-*.md 13-*.md 14-*.md 15-*.md 16-*.md 17-*.md 18-*.md 19-*.md && git commit -m "Add PHP control flow lessons"`.

### Task 3: Function lessons

**Files:** Create `20-creating-functions.md` through `27-function-scope.md`.

- [ ] Cover declaration, parameters, return values, defaults, type declarations, anonymous and arrow functions, and local/global/static scope in eight standalone files.
- [ ] Use `declare(strict_types=1);` where it clarifies scalar type declarations.
- [ ] Verify lesson count: `rg -l '^# ' 2[0-7]-*.md | Measure-Object`.
- [ ] Commit: `git add 2[0-7]-*.md && git commit -m "Add PHP function lessons"`.

### Task 4: Arrays and strings lessons

**Files:** Create `28-indexed-arrays.md` through `34-explode-and-implode.md`.

- [ ] Cover indexed, associative, and multidimensional arrays; array functions; manipulation; string functions; and `explode`/`implode` in seven files.
- [ ] Show inputs and output using `var_dump`, `print_r`, or clear `echo` output when useful.
- [ ] Verify no duplicate headings: `rg '^# ' 2[8-9]-*.md 3[0-4]-*.md`.
- [ ] Commit: `git add 2[8-9]-*.md 3[0-4]-*.md && git commit -m "Add PHP arrays and strings lessons"`.

### Task 5: Forms, input, and superglobals lessons

**Files:** Create `35-html-forms-with-php.md` through `46-env.md`.

- [ ] Create standalone lessons for forms, GET, POST, REQUEST, validation, sanitization, file uploads, and each requested superglobal (`GET`, `POST`, `SESSION`, `COOKIE`, `FILES`, `SERVER`, `ENV`).
- [ ] Use an HTML form plus PHP handler where needed; explain that `REQUEST` mixes sources and is less explicit than GET/POST.
- [ ] Include upload checks for error code, size, MIME type, and `move_uploaded_file`; never trust user-provided filenames or MIME declarations alone.
- [ ] Verify all twelve files: `rg -l '^# ' 3[5-9]-*.md 4[0-6]-*.md`.
- [ ] Commit: `git add 3[5-9]-*.md 4[0-6]-*.md && git commit -m "Add PHP forms and superglobals lessons"`.

### Task 6: Include and file handling lessons

**Files:** Create `47-include.md`, `48-require.md`, `49-include-once.md`, `50-require-once.md`, `51-reading-files.md`, `52-writing-files.md`, `53-json-handling.md`.

- [ ] Explain failure behavior for each inclusion construct and demonstrate safe reading/writing with error checks.
- [ ] Use `json_encode` and `json_decode` examples with JSON error handling.
- [ ] Verify seven files: `rg -l '^# ' 4[7-9]-*.md 5[0-3]-*.md`.
- [ ] Commit: `git add 4[7-9]-*.md 5[0-3]-*.md && git commit -m "Add PHP file handling lessons"`.

### Task 7: Object-oriented PHP lessons

**Files:** Create `54-classes-and-objects.md` through `65-exception-handling.md`.

- [ ] Cover classes/objects, properties/methods, constructors, inheritance, encapsulation, interfaces, abstract classes, traits, static members, namespaces, autoloading, and exceptions in twelve focused files.
- [ ] Use a consistent `App` namespace in namespace/autoloading examples and `try`/`catch`/`finally` in exception examples.
- [ ] Verify all files: `rg -l '^# ' 5[4-9]-*.md 6[0-5]-*.md`.
- [ ] Commit: `git add 5[4-9]-*.md 6[0-5]-*.md && git commit -m "Add object-oriented PHP lessons"`.

### Task 8: Database lessons

**Files:** Create `66-database-fundamentals.md`, `67-tables.md`, `68-crud.md`, `69-sql-basics.md`, `70-pdo.md`, `71-prepared-statements.md`, `72-relationships.md`, `73-transactions.md`.

- [ ] Teach MySQL concepts and SQL with focused examples; use PDO exceptions and parameter binding for all data supplied by users.
- [ ] Explain primary/foreign keys and demonstrate `beginTransaction`, `commit`, and `rollBack`.
- [ ] Verify eight files: `rg -l '^# ' 6[6-9]-*.md 7[0-3]-*.md`.
- [ ] Commit: `git add 6[6-9]-*.md 7[0-3]-*.md && git commit -m "Add PHP database lessons"`.

### Task 9: Authentication lessons

**Files:** Create `74-registration.md`, `75-login-and-logout.md`, `76-password-hashing.md`, `77-sessions.md`, `78-authorization.md`, `79-basic-security-practices.md`.

- [ ] Demonstrate registration and login flow, `password_hash`, `password_verify`, session regeneration, role checks, CSRF awareness, and secure-cookie guidance.
- [ ] Clearly label examples as educational and explain production requirements such as HTTPS and rate limiting.
- [ ] Verify six files: `rg -l '^# ' 7[4-9]-*.md`.
- [ ] Commit: `git add 7[4-9]-*.md && git commit -m "Add PHP authentication lessons"`.

### Task 10: Modern PHP lessons

**Files:** Create `80-composer.md`, `81-packages.md`, `82-psr-standards.md`, `83-modern-namespaces.md`, `84-modern-autoloading.md`, `85-env-files.md`, `86-mvc-architecture.md`, `87-rest-api-basics.md`, `88-http-methods.md`, `89-json-apis.md`.

- [ ] Explain Composer commands, package constraints, PSR-4, `.env` loading without committing secrets, MVC boundaries, REST resource design, HTTP methods/status codes, and JSON API headers/errors.
- [ ] Keep `83` and `84` focused on their modern-application context without duplicating OOP lesson content.
- [ ] Verify ten files: `rg -l '^# ' 8[0-9]-*.md`.
- [ ] Commit: `git add 8[0-9]-*.md && git commit -m "Add modern PHP lessons"`.

### Task 11: Course index and full validation

**Files:** Modify `readme.md`.

- [ ] Replace the existing overview with an ordered table of contents linking every `01` through `89` lesson exactly once.
- [ ] Validate lesson count and README targets with:

```powershell
$lessons = Get-ChildItem -File -Filter '*.md' | Where-Object { $_.Name -match '^\d{2}-' }
if ($lessons.Count -ne 89) { throw "Expected 89 lesson files; found $($lessons.Count)" }
$missing = $lessons | Where-Object { (Get-Content -Raw 'readme.md') -notmatch [regex]::Escape($_.Name) }
if ($missing) { throw "README is missing links: $($missing.Name -join ', ')" }
$fenceIssues = $lessons | Where-Object { ((Select-String -Path $_.FullName -Pattern '^```' | Measure-Object).Count % 2) -ne 0 }
if ($fenceIssues) { throw "Unbalanced code fences: $($fenceIssues.Name -join ', ')" }
```

- [ ] Commit and publish: `git add readme.md && git commit -m "Add PHP course index" && git push`.
