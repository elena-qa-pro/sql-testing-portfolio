# API Test Scenarios

---

## TC-API-001 Valid GET Request

Request:
GET /users/1

Expected:
Status 200 OK
Response contains user data
Response time < 2 seconds

---

## TC-API-002 Invalid Endpoint

Request:
GET /invalid-url

Expected:
Status 404 Not Found

---

## TC-API-003 Unauthorized Request

Request:
GET /users
(no auth token)

Expected:
Status 401 Unauthorized

---

## TC-API-004 Invalid JSON Body

Request:
POST /users
Body: malformed JSON

Expected:
Status 400 Bad Request

---

## TC-API-005 Data Validation

Request:
POST /users
Body:
{
 "email": "invalid_email"
}

Expected:
Validation error returned
-test-scenario
