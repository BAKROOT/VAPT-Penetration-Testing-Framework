# API Security Testing Checklist

Aligned with the OWASP API Security Top 10. Applies to REST and GraphQL APIs. Mark each item Pass / Fail / N/A / Review and log failures as findings.

## Discovery & Documentation
- [ ] Obtain/derive API documentation (OpenAPI/Swagger, GraphQL schema)
- [ ] Enumerate endpoints, methods, and parameters
- [ ] Identify API versions and deprecated endpoints
- [ ] Identify authentication mechanism (API key, OAuth, JWT)

## Broken Object Level Authorization (BOLA/IDOR)
- [ ] Test access to other users' objects by changing IDs
- [ ] Test object-level authorization on every endpoint
- [ ] Test nested/related object access

## Broken Authentication
- [ ] Test for weak or missing authentication
- [ ] Test JWT handling (signature, alg=none, expiry, secret strength)
- [ ] Test token leakage and reuse
- [ ] Test credential stuffing/brute-force protections

## Broken Object Property Level Authorization
- [ ] Test for mass assignment / excessive data exposure
- [ ] Verify responses do not return sensitive fields
- [ ] Test ability to modify restricted properties

## Resource Consumption
- [ ] Test for missing rate limiting / throttling
- [ ] Test for resource exhaustion (large payloads, pagination abuse)
- [ ] Test GraphQL query depth/complexity limits

## Broken Function Level Authorization
- [ ] Test access to administrative functions as a normal user
- [ ] Test HTTP method tampering (GET vs POST vs DELETE)

## Server-Side Request Forgery
- [ ] Test parameters that fetch remote resources for SSRF

## Security Misconfiguration
- [ ] Review CORS configuration
- [ ] Verify security headers on API responses
- [ ] Check for verbose error messages and stack traces
- [ ] Verify TLS enforced on all endpoints

## Injection
- [ ] Test for SQL/NoSQL injection in parameters
- [ ] Test for command/template injection
- [ ] Test GraphQL injection and introspection exposure

## Improper Inventory Management
- [ ] Identify shadow/undocumented endpoints
- [ ] Identify non-production endpoints reachable in prod
