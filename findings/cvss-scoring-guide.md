# CVSS v3.1 Scoring Guide

All findings are scored using the Common Vulnerability Scoring System (CVSS) v3.1. This guide explains the base metrics and how scores map to qualitative severity bands.

## Qualitative Severity Bands

| CVSS Base Score | Severity |
| --- | --- |
| 0.0 | None / Informational |
| 0.1 – 3.9 | Low |
| 4.0 – 6.9 | Medium |
| 7.0 – 8.9 | High |
| 9.0 – 10.0 | Critical |

## Base Metric Groups

### Exploitability metrics
- **Attack Vector (AV):** Network (N), Adjacent (A), Local (L), Physical (P)
- **Attack Complexity (AC):** Low (L), High (H)
- **Privileges Required (PR):** None (N), Low (L), High (H)
- **User Interaction (UI):** None (N), Required (R)

### Scope
- **Scope (S):** Unchanged (U), Changed (C)

### Impact metrics
- **Confidentiality (C):** None (N), Low (L), High (H)
- **Integrity (I):** None (N), Low (L), High (H)
- **Availability (A):** None (N), Low (L), High (H)

## Vector String Format

`CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H`

Each finding in `findings-register.csv` must include both the numeric score and the full vector string so the rating is transparent and reproducible.

## Worked Examples

| Scenario | Example vector | Score | Severity |
| --- | --- | --- | --- |
| Unauthenticated remote SQL injection (full impact) | AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H | 9.8 | Critical |
| Stored XSS requiring victim interaction | AV:N/AC:L/PR:L/UI:R/S:C/C:H/I:L/A:N | 7.4 | High |
| Missing rate limiting (limited availability impact) | AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:L | 5.3 | Medium |
| Verbose error disclosure | AV:N/AC:H/PR:N/UI:N/S:U/C:L/I:N/A:N | 3.7 | Low |

## Adjusting for Context

Base scores can be refined with Temporal and Environmental metrics where appropriate (e.g., exploit maturity, compensating controls, asset criticality). Document any environmental adjustment and the rationale in the finding.

## Reference

- Use the official FIRST CVSS v3.1 calculator to derive scores, and record the resulting vector string with every finding.
