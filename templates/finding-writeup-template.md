# Finding Write-up — Template

> Use this structure for every finding. Replace all `[bracketed]` fields. Keep evidence sanitized.

---

## [F-XXX] — [Concise Finding Title]

| Field | Value |
| --- | --- |
| **Finding ID** | F-XXX |
| **Severity** | [Critical / High / Medium / Low / Informational] |
| **CVSS v3.1** | [score] ([vector string]) |
| **Category** | [e.g., Injection, Broken Access Control] |
| **CWE** | [CWE-XX] |
| **Affected asset(s)** | [URL / host / endpoint] |
| **Status** | [Open / Remediated / Risk accepted] |

### Description
[Clear explanation of the vulnerability and why it exists.]

### Impact
[What an attacker could achieve; the business and technical consequences.]

### Steps to Reproduce
1. [step]
2. [step]
3. [step]

### Evidence
[Sanitized screenshots, request/response snippets, or command output. Do not include real sensitive data.]

```
[sanitized proof-of-concept / request]
```

### Remediation
[Specific, actionable guidance to fix the issue. Include configuration or code-level recommendations.]

### References
- [OWASP / CWE / vendor advisory links]

---

### Severity Guidance
- **Critical** — direct, high-impact compromise (e.g., RCE, full data breach).
- **High** — significant impact, likely exploitable.
- **Medium** — moderate impact or requires conditions.
- **Low** — limited impact.
- **Informational** — best-practice or hardening note, no direct risk.
