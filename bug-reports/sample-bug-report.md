# Bug Report — Incorrect Total Calculation

## Bug ID
BR-001

## Title
Order total is calculated incorrectly when discount applied

## Severity
High

## Priority
High

## Environment
Production

## Preconditions
User is logged in  
Cart contains 2+ items  
Discount code applied

---

## Steps to Reproduce
1. Add item A ($50)
2. Add item B ($50)
3. Apply 10% discount
4. Proceed to checkout

---

## Expected Result
Total should be $90

---

## Actual Result
Total displayed is $100

---

## Impact
User is charged incorrect amount which may lead to customer complaints and financial discrepancies.

---

## Root Cause (Hypothesis)
Discount not applied during backend calculation.

---

## Attachments
Screenshots / logs / request payloads (if available)
