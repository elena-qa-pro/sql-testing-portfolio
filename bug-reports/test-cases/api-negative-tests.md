# API Negative Test Scenarios

---

## TC-API-001 Missing Required Field

Request:
POST /users

Payload:
{
  "email": ""
}

Expected Result:
400 Bad Request returned  
Error message: "Email is required"

---

## TC-API-002 Invalid Data Type

Payload:
{
  "age": "twenty"
}

Expected Result:
Validation error returned.

---

## TC-API-003 Unauthorized Access

Request:
GET /users

Without token

Expected Result:
401 Unauthorized

---

## TC-API-004 Expired Token

Steps:
1. Send request with expired token

Expected Result:
401 Token expired

---

## TC-API-005 Invalid Endpoint

Request:
GET /userzzz

Expected Result:
404 Not Found
