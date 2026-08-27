# PHP Fundamentals Lessons Design

## Goal

Create a beginner-to-pre-Laravel PHP curriculum from the topics supplied by the user. Each listed subject becomes one standalone Markdown file, so learners can study or link to a concept independently.

## File Architecture

All lesson files live at the repository root and use a stable numerical prefix followed by a lowercase, hyphenated topic name. The prefix preserves the intended learning sequence; the filename makes each subject easy to locate.

Every file covers exactly one listed topic. A lesson contains:

1. a short explanation of the concept and why it matters;
2. syntax or conceptual rules;
3. one or more complete PHP examples;
4. expected output, use notes, or security guidance when applicable; and
5. concise common pitfalls when they materially aid learning.

The existing `readme.md` becomes a course table of contents linking to every lesson. It is navigation only; it does not duplicate lessons.

## Content Boundaries

Examples target modern PHP 8+ and use plain PHP unless a subject inherently requires HTML, MySQL, Composer, or HTTP. Database examples use PDO and prepared statements. Security-oriented lessons demonstrate input validation, output escaping, password hashing, session handling, and authorization boundaries without presenting insecure patterns as production-ready.

The course covers PHP fundamentals, control flow, functions, arrays and strings, forms and input, superglobals, file handling, OOP, database access, authentication, and modern PHP concepts required before Laravel.

## Verification

Before publication, verify that every user-listed topic maps to exactly one lesson file, filenames are unique and sequential, Markdown code fences are balanced, internal README links resolve, and the repository has a clean Git status after committing and pushing the lessons.
