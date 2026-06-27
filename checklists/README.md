# Testing Checklists

Domain-specific checklists used during the Vulnerability Analysis and Exploitation phases. Each checklist is aligned to recognized standards and is meant to ensure consistent coverage across engagements.

## Contents

| File | Domain | Primary standard |
| --- | --- | --- |
| `web-application-checklist.md` | Web applications | OWASP WSTG / Top 10 |
| `network-infrastructure-checklist.md` | Network & infrastructure | NIST SP 800-115 / OSSTMM |
| `api-security-checklist.md` | REST/GraphQL APIs | OWASP API Security Top 10 |
| `mobile-application-checklist.md` | iOS / Android apps | OWASP MASVS / MASTG |
| `cloud-security-checklist.md` | Cloud (AWS/Azure/GCP) | CIS Benchmarks / cloud best practice |

## How to Use

1. Pick the checklist matching the in-scope target.
2. Work through each item, marking status (Pass / Fail / N/A / Needs review).
3. Log any failure as a finding in `findings/findings-register.csv`.
4. Reference the checklist item ID in the finding for traceability.

## Status Legend

- **Pass** — control present / no issue found.
- **Fail** — issue identified (create a finding).
- **N/A** — not applicable to this target.
- **Review** — needs manual follow-up.
