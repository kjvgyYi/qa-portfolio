# Bug Reports
# BUG-002 — Silent failure on spaces-only First Name input

**Date:** April 2026  
**Tester:** Hlib Klipko  
**URL:** https://demo.opencart.com/index.php?route=account/register

---

| Field | Details |
|-------|---------|
| **Severity** | Major |
| **Priority** | High |
| **Status** | Open |
| **Type** | Validation Bug / UX Bug |

---

## Description
When spaces-only input is entered in the First Name field and the user
clicks "Continue", the form does nothing — no error message, no redirect,
no visual feedback. The user has no way to understand why the form is not
submitting. This is a "silent failure" — one of the worst UX patterns.

---

## Steps to Reproduce
1. Open: https://demo.opencart.com/index.php?route=account/register
2. Click on First Name field and enter 5-6 spaces: `      `
3. Enter Last Name: `Smith`
4. Enter Email: any valid unique email
5. Enter Password: `Test1234!`
6. Enable "I have read and agree to the Privacy Policy" toggle
7. Click "Continue"

---

## Expected Result
Form displays a clear validation error message under the First Name field:
> "First Name must not be empty or contain only spaces"

## Actual Result
Nothing happens. Form stays on the same page with no error message,
no highlighted field, no user feedback of any kind.

---

## Screenshot
![BUG-002 Screenshot](BUG-002-screenshot.png)

---

## Environment
- **Browser:** Chrome (latest)
- **OS:** Windows
- **Test URL:** https://demo.opencart.com

---

## Severity Justification
Silent failures break user trust and increase support requests.
Users cannot complete registration and don't know why.
Standard UX practice requires explicit validation messages on all
required fields with invalid input.
