# Tables

A table defines columns, their types, and rules for a set of related records. A primary key uniquely identifies each row.

```sql
CREATE TABLE students (
  id BIGINT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(255) NOT NULL UNIQUE,
  created_at TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP
);
```

Run the SQL in a MySQL client to create an empty `students` table.

`NOT NULL` requires a value and `UNIQUE` prevents duplicate emails.

Pitfall: choose column types and lengths deliberately. Do not store passwords in plain text or rely on client-side validation for constraints.
