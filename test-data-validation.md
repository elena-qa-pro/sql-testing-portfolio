# SQL Data Validation Test Cases

## Objective
Validate data integrity between application layer and database to ensure accuracy, consistency, and reliability of stored data.

---

## Test Scenario 1 — Record Creation Validation
**Purpose:** Verify that new records are correctly stored in database after API request.

SQL:
SELECT * FROM users WHERE id = 101;

Expected Result:
Record exists and matches submitted payload values.

---

## Test Scenario 2 — Data Consistency Check
**Purpose:** Ensure UI values match database values.

SQL:
SELECT email, status FROM users WHERE id = 101;

Expected Result:
Values match UI display.

---

## Test Scenario 3 — Null Constraint Validation
**Purpose:** Confirm required fields are not saved as NULL.

SQL:
SELECT * FROM users WHERE email IS NULL;

Expected Result:
No records returned.

---

## Test Scenario 4 — Duplicate Record Detection
**Purpose:** Validate system prevents duplicate entries.

SQL:
SELECT email, COUNT(*)
FROM users
GROUP BY email
HAVING COUNT(*) > 1;

Expected Result:
No duplicates returned.

---

## Test Scenario 5 — Data Type Validation
**Purpose:** Ensure numeric fields contain valid numeric data.

SQL:
SELECT * FROM orders WHERE total_amount < 0;

Expected Result:
No invalid negative values.

---

## Test Scenario 6 — Referential Integrity Check
**Purpose:** Ensure foreign key relationships are valid.

SQL:
SELECT *
FROM orders o
LEFT JOIN users u ON o.user_id = u.id
WHERE u.id IS NULL;

Expected Result:
No orphan records.

---

## Tools Used
- SQL queries
- Database console
- Application logs
- API responses

---

## Validation Focus
- Accuracy
- Integrity
- Consistency
- Constraints
- Relationships
