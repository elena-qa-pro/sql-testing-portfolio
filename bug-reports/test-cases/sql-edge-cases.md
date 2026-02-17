# SQL Edge Case Test Scenarios

---

## TC-SQL-001 NULL Value Handling

Objective:
Verify system behavior when database fields contain NULL values.

Steps:
1. Insert record with NULL in optional field
2. Retrieve record via query
3. Validate response

Expected Result:
System handles NULL correctly without crash or incorrect data mapping.

---

## TC-SQL-002 Duplicate Record Detection

Objective:
Ensure system prevents duplicate entries.

Steps:
1. Insert record
2. Insert same record again

Expected Result:
Database rejects duplicate OR system flags validation error.

---

## TC-SQL-003 Data Type Mismatch

Objective:
Validate database rejects invalid data types.

Steps:
1. Insert string into integer column

Expected Result:
Query fails with type validation error.

---

## TC-SQL-004 Boundary Value Testing

Objective:
Verify DB accepts only allowed limits.

Steps:
1. Insert max allowed value
2. Insert value exceeding limit

Expected Result:
Max accepted  
Overflow rejected

---

## TC-SQL-005 Orphan Record Validation

Objective:
Check foreign key integrity.

Steps:
1. Insert child record without parent

Expected Result:
Foreign key constraint prevents insert.
