# Payment Test Cases

---

## TC-PAY-001 Successful Payment

Preconditions:  
User is logged in and has items in cart.

Steps:
1. Open checkout page
2. Enter valid card number
3. Enter valid expiration date
4. Enter valid CVV
5. Click Pay

Expected Result:  
Payment is successful and confirmation page is displayed.

---

## TC-PAY-002 Invalid Card Number

Steps:
1. Enter invalid card number
2. Enter valid expiration date
3. Enter valid CVV
4. Click Pay

Expected Result:  
Error message displayed: "Invalid card number"

---

## TC-PAY-003 Expired Card

Steps:
1. Enter valid card number
2. Enter expired date
3. Enter valid CVV
4. Click Pay

Expected Result:  
Error message displayed: "Card expired"

---

## TC-PAY-004 Empty Fields Validation

Steps:
1. Leave all fields empty
2. Click Pay

Expected Result:  
Validation messages displayed for required fields.

---

## TC-PAY-005 Network Failure During Payment

Steps:
1. Enter valid payment data
2. Disable internet connection
3. Click Pay

Expected Result:  
Payment fails gracefully with message:
"Network error. Please try again."

---

## TC-PAY-006 Duplicate Payment Prevention

Steps:
1. Enter valid payment details
2. Click Pay multiple times quickly

Expected Result:  
Only one transaction processed. No duplicate charge.

---

## TC-PAY-007 Currency Validation

Steps:
1. Change currency during checkout
2. Proceed to payment

Expected Result:  
Correct currency and amount processed.
