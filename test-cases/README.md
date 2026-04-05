# Test Cases
# Test Cases — Registration Form
**URL:** https://demo.opencart.com/index.php?route=account/register  
**Date:** April 2026  
**Tester:** Hlib Klipko

---

## TC-001 — Successful registration with valid data
**Priority:** High | **Severity:** Critical

**Steps:**
1. Open registration page
2. Enter First Name: `John`
3. Enter Last Name: `Smith`
4. Enter Email: `john.smith.test01@gmail.com`
5. Enter Password: `Test1234!`
6. Click "Continue"

**Expected:** Account created, redirect to success page  
**Actual:** Account created successfully, redirected to success page  
**Status:** ✅ Pass

---

## TC-002 — Registration with empty First Name
**Priority:** High | **Severity:** Major

**Steps:**
1. Open registration page
2. Leave First Name empty
3. Fill all other fields with valid data
4. Click "Continue"

**Expected:** Error message shown under First Name field  
**Actual:** Error message displayed — "First Name must be between 1 and 32 characters"  
**Status:** ✅ Pass

---

## TC-003 — Registration with invalid email format
**Priority:** High | **Severity:** Major

**Steps:**
1. Open registration page
2. Enter Email: `notanemail`
3. Fill all other fields with valid data
4. Click "Continue"

**Expected:** Error message "E-Mail Address does not appear to be valid"  
**Actual:** Error message displayed — "E-Mail Address does not appear to be valid"  
**Status:** ✅ Pass

---

## TC-004 — Registration with already existing email
**Priority:** High | **Severity:** Major

**Steps:**
1. Open registration page
2. Enter Email that was already registered
3. Fill all other fields with valid data
4. Click "Continue"

**Expected:** Error message "Warning: E-Mail Address is already registered"  
**Actual:** Warning displayed — "Warning: E-Mail Address is already registered"  
**Status:** ✅ Pass

---

## TC-005 — Password too short (boundary value)
**Priority:** Medium | **Severity:** Major

**Steps:**
1. Open registration page
2. Enter Password: `Ab1!` (4 characters)
3. Fill all other fields with valid data
4. Click "Continue"

**Expected:** Error message about minimum password length  
**Actual:** Registration accepted. Password between 4-20 characters is allowed  
**Status:** ✅ Pass

---

## TC-006 — Registration with spaces in First Name
**Priority:** Low | **Severity:** Minor

**Steps:**
1. Open registration page
2. Enter First Name: `   ` (only spaces)
3. Fill all other fields with valid data
4. Click "Continue"

**Expected:** Error — spaces-only input should not be accepted  
**Actual:** Form silently blocks submission with no error message displayed  
**Status:** ❌ Fail — see BUG-001, BUG-002

---

## TC-007 — First Name maximum length (boundary value)
**Priority:** Low | **Severity:** Minor

**Steps:**
1. Open registration page
2. Enter First Name: 33 characters — `Aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa`
3. Fill all other fields with valid data
4. Click "Continue"

**Expected:** Error or field limits input to 32 characters  
**Actual:** Error displayed — input limited to 32 characters  
**Status:** ✅ Pass
