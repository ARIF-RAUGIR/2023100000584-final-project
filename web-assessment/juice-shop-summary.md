# OWASP Juice Shop — Web Application Assessment Summary

**Room:** OWASP Juice Shop (TryHackMe)
---

## Tasks Completed

- Authentication bypass testing
- SQL Injection exploitation
- Cross-Site Scripting (XSS) testing
- Weak authentication analysis

---

## Key Findings

### 1. SQL Injection — Login Bypass
- **Severity:** Critical
- Crafted payload in login form bypassed authentication entirely
- Admin account accessed without valid credentials

### 2. Cross-Site Scripting (XSS) — Reflected
- **Severity:** High
- Script payload injected via search field executed in browser
- Application does not sanitize user input before rendering

### 3. Weak Authentication — Insecure Password Policy
- **Severity:** Medium
- Application accepted weak and easily guessable passwords
- No account lockout mechanism observed

---

## Security Impact

These vulnerabilities can lead to unauthorized account access, session hijacking, data exfiltration, and full application compromise.

---

## Remediation Recommendations

- Use parameterized queries for all database interactions
- Implement output encoding and Content Security Policy (CSP)
- Enforce strong password policy and account lockout
- Implement Multi-Factor Authentication (MFA)
- Validate and sanitize all user-supplied input
