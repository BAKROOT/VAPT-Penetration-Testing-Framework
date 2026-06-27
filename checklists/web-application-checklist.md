# Web Application Testing Checklist

Aligned with the OWASP Web Security Testing Guide (WSTG) and the OWASP Top 10. Mark each item Pass / Fail / N/A / Review and log failures as findings.

## Information Gathering
- [ ] Fingerprint web server, frameworks, and technologies
- [ ] Review robots.txt, sitemap, and metadata for exposed paths
- [ ] Enumerate application entry points and endpoints
- [ ] Identify and map application functionality and roles

## Configuration & Deployment
- [ ] Check for default/sample files and admin interfaces
- [ ] Review HTTP security headers (HSTS, CSP, X-Content-Type-Options)
- [ ] Test TLS configuration and certificate validity
- [ ] Check for verbose errors and stack traces

## Authentication
- [ ] Test for weak or default credentials
- [ ] Test account lockout and brute-force protections
- [ ] Test password reset and recovery flows
- [ ] Test multi-factor authentication (where present)
- [ ] Check credentials transmitted only over TLS

## Session Management
- [ ] Verify session cookie attributes (Secure, HttpOnly, SameSite)
- [ ] Test session fixation and session invalidation on logout
- [ ] Test session timeout enforcement
- [ ] Test CSRF protections on state-changing requests

## Authorization
- [ ] Test for insecure direct object references (IDOR)
- [ ] Test horizontal and vertical privilege escalation
- [ ] Test for forced browsing to restricted resources
- [ ] Verify access control enforced server-side

## Input Validation
- [ ] Test for SQL injection
- [ ] Test for cross-site scripting (reflected, stored, DOM)
- [ ] Test for command injection
- [ ] Test for server-side template injection (SSTI)
- [ ] Test for XML external entity (XXE) injection
- [ ] Test for server-side request forgery (SSRF)
- [ ] Test for open redirects
- [ ] Test for file upload vulnerabilities

## Business Logic
- [ ] Test for logic flaws and workflow bypasses
- [ ] Test for race conditions on critical operations
- [ ] Test for parameter and price/quantity tampering

## Client-Side
- [ ] Review client-side storage for sensitive data
- [ ] Test for DOM-based vulnerabilities
- [ ] Review third-party scripts and subresource integrity

## Cryptography & Data Protection
- [ ] Verify sensitive data encrypted in transit and at rest
- [ ] Check for hard-coded secrets in client-side code
- [ ] Review use of strong, current cryptographic algorithms

## Error Handling & Logging
- [ ] Verify errors do not leak sensitive information
- [ ] Confirm security events are logged appropriately
