# Login Test Cases

---

## TC-001 Valid Login

Preconditions:
User exists in system

Steps:
1. Open login page
2. Enter valid email
3. Enter valid password
4. Click Login

Expected Result:
User successfully logged in and redirected to dashboard.

---

## TC-002 Invalid Password

Steps:
1. Enter valid email
2. Enter incorrect password
3. Click Login

Expected Result:
Error message displayed: "Invalid credentials"

---

## TC-003 Empty Fields

Steps:
1. Leave email empty
2. Leave password empty
3. Click Login

Expected Result:
Validation errors displayed for required fields.
