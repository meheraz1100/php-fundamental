# Relationships

Relationships connect records across tables. A foreign key records that one row belongs to another and lets the database enforce that reference.

```sql
CREATE TABLE orders (
  id BIGINT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
  customer_id BIGINT UNSIGNED NOT NULL,
  total DECIMAL(10,2) NOT NULL,
  CONSTRAINT fk_orders_customer FOREIGN KEY (customer_id) REFERENCES customers(id)
);
```

This creates a one-to-many relationship: one customer can have many orders.

Common relationship types are one-to-one, one-to-many, and many-to-many (usually modeled with a junction table).

Tip: index foreign-key columns for efficient joins, and decide deliberately whether deletes should restrict, cascade, or set a reference to null.
