# API Testing — JSONPlaceholder
**Base URL:** https://jsonplaceholder.typicode.com  
**Tool:** Postman  
**Date:** April 2026  
**Tester:** Hlib Klipko

---

## Test Results

| ID | Method | Endpoint | Expected Status | Actual Status | Result |
|----|--------|----------|-----------------|---------------|--------|
| API-001 | GET | /posts | 200 OK | 200 OK | ✅ Pass |
| API-002 | GET | /posts/1 | 200 OK | 200 OK | ✅ Pass |
| API-003 | GET | /posts/99999 | 404 Not Found | 404 Not Found | ✅ Pass |
| API-004 | GET | /posts/1/comments | 200 OK | 200 OK | ✅ Pass |
| API-005 | POST | /posts | 201 Created | 201 Created | ✅ Pass |

---

## Response Examples

**GET /posts/1 — Response:**
```json
{
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit suscipit..."
}
```

**GET /posts/99999 — Response:**
```json
{}
```
> Empty object returned with 404 status — resource not found confirmed.
