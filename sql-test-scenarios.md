# SQL Test Scenarios

## Objective
Validate database integrity, accuracy, and data consistency through SQL validation testing.

---

## Test Scenario 1 — Verify record creation

Query:
SELECT * FROM users WHERE id = 101;

Expected Result:
Record exists and matches input data.

---

## Test Scenario 2 — Validate NULL constraints

Query:
INSERT INTO users (name) VALUES (NULL);

Expected Result:
Database rejects insert if column is NOT NULL.

---

## Test Scenario 3 — Data consistency check

Query:
SELECT COUNT(*) FROM orders WHERE user_id NOT IN (SELECT id FROM users);

Expected Result:
Result = 0

---

## Test Scenario 4 — Duplicate prevention

Query:
SELECT email, COUNT(*) 
FROM users 
GROUP BY email 
HAVING COUNT(*) > 1;

Expected Result:
No duplicate emails returned.

---

## Test Scenario 5 — Boundary value validation

Query:
SELECT * FROM payments WHERE amount < 0;

Expected Result:
No records returned.
