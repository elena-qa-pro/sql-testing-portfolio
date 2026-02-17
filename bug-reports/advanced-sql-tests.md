# Advanced SQL Validation Test Cases

---

## TC-101 Duplicate Records Detection

Purpose: Verify system does not allow duplicate users.

Query:
SELECT email, COUNT(*)
FROM users
GROUP BY email
HAVING COUNT(*) > 1;

Expected Result:
Query returns zero rows.

---

## TC-102 Null Values Validation

Purpose: Ensure required fields are not null.

Query:
SELECT *
FROM orders
WHERE order_id IS NULL
   OR customer_id IS NULL;

Expected Result:
No records returned.

---

## TC-103 Data Consistency Between Tables

Purpose: Validate referential integrity between tables.

Query:
SELECT orders.customer_id
FROM orders
LEFT JOIN customers
ON orders.customer_id = customers.id
WHERE customers.id IS NULL;

Expected Result:
Zero rows returned.

---

## TC-104 Aggregation Accuracy Check

Purpose: Verify totals match calculated values.

Query:
SELECT
SUM(price * quantity) AS calculated_total,
SUM(total_amount) AS stored_total
FROM order_items;

Expected Result:
calculated_total = stored_total

---

## TC-105 Invalid Data Detection

Purpose: Detect invalid business values.

Query:
SELECT *
FROM payments
WHERE amount < 0;

Expected Result:
No negative values.

---

## TC-106 Date Validation

Purpose: Verify logical date sequence.

Query:
SELECT *
FROM subscriptions
WHERE end_date < start_date;

Expected Result:
No records returned.

---

## Notes
These tests validate:
- Data integrity
- Referential consistency
- Aggregation correctness
- Business logic rules
