# FUTURE_CS_03
# API Security Risk Analysis: JSONPlaceholder (2026)


## Overview

This repository contains a professional API Security Risk Analysis conducted against JSONPlaceholder, a public REST API used for testing and prototyping. The assessment was performed following OWASP API Security Top 10 (2023) guidelines using an ethical, read-only methodology.

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Postman (Lightweight Client) | Endpoint testing and response inspection |
| Browser DevTools | Header analysis |
| OWASP API Security Top 10 (2023) | Risk classification framework |

---

## Scope

**Target API:** https://jsonplaceholder.typicode.com  

**Endpoints Tested:**
- `GET /users` - unauthenticated user data access
- `GET /users/{id}` - object-level authorization test
- `GET /posts` - unauthenticated content access
- `POST /posts` - unauthenticated write access test
- Response headers - security header inspection

**Not in scope:** exploitation, DoS testing, or any private/production systems.

---

## Methodology

1. API documentation review
2. Endpoint enumeration via Postman
3. Authentication and authorization testing
4. Response data analysis for excessive exposure
5. Security response header inspection
6. Risk classification using OWASP API Security Top 10

---

## Findings Summary

| Risk ID | Title | Severity | OWASP Ref |
|---------|-------|----------|-----------|
| R-01 | Unauthenticated Access to User Data | 🔴 HIGH | API1:2023 |
| R-02 | Broken Object Level Authorization (IDOR) | 🔴 HIGH | API1:2023 |
| R-03 | Unauthenticated Write Access | 🟡 MEDIUM | API5:2023 |
| R-04 | Missing Security Response Headers | 🟡 MEDIUM | API7:2023 |
| R-05 | Technology Stack Disclosure | 🟢 LOW | API8:2023 |

---

## ⚠️ Disclaimer

This assessment was conducted solely for educational purposes against a public demo API explicitly provided for testing. No production systems were targeted. No data was exfiltrated, modified, or deleted. All testing followed ethical guidelines.

---

## 🔗 References

- [OWASP API Security Top 10](https://owasp.org/API-Security/)
- [JSONPlaceholder](https://jsonplaceholder.typicode.com)
