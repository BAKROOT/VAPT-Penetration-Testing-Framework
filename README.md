# VAPT — Vulnerability Assessment and Penetration Testing Framework

A complete, end-to-end **Vulnerability Assessment and Penetration Testing (VAPT)** framework. This repository provides the methodology, planning artifacts, testing checklists, reporting templates, and remediation tracking needed to plan, execute, and deliver professional security assessments in a consistent, repeatable, and ethical way.

> **Authorized testing only.** Every engagement in this framework requires written authorization. Never test systems you do not own or do not have explicit, signed permission to assess.

---

## What is VAPT?

Vulnerability Assessment (VA) is the systematic identification, classification, and prioritization of security weaknesses. Penetration Testing (PT) goes further by safely exploiting weaknesses to demonstrate real-world impact. Together, VAPT gives an organization both breadth (what is exposed) and depth (what an attacker could actually achieve).

---

## Repository Structure

| Path | Purpose |
| --- | --- |
| `methodology/` | Testing methodology, phases, and recognized standards (OWASP, PTES, NIST, OSSTMM) |
| `scope-rules-of-engagement/` | Rules of Engagement (ROE), authorization, and scoping templates |
| `checklists/` | Per-domain testing checklists: web, network, API, mobile, cloud |
| `templates/` | Report template, executive summary, and findings write-up format |
| `findings/` | Findings register and severity/CVSS scoring guidance |
| `remediation/` | Remediation tracker and retest verification process |
| `tools/` | Curated tooling reference by phase and domain |
| `reporting/` | Reporting standards, evidence handling, and deliverable checklist |

---

## Assessment Lifecycle

1. **Pre-engagement** — scoping, authorization, ROE sign-off.
2. **Reconnaissance** — passive and active information gathering.
3. **Scanning & Enumeration** — service discovery and vulnerability identification.
4. **Exploitation** — controlled validation of findings.
5. **Post-exploitation** — impact analysis (within authorized scope).
6. **Reporting** — findings, evidence, risk ratings, and remediation guidance.
7. **Remediation & Retest** — verify fixes and close findings.

---

## Standards Referenced

- **OWASP** — Web Security Testing Guide (WSTG), API Security Top 10, MASVS (mobile).
- **PTES** — Penetration Testing Execution Standard.
- **NIST SP 800-115** — Technical Guide to Information Security Testing.
- **OSSTMM** — Open Source Security Testing Methodology Manual.
- **CVSS v3.1** — Common Vulnerability Scoring System for severity ratings.

---

## How to Use This Repository

Start with `scope-rules-of-engagement/` to define and authorize the engagement, follow the relevant checklist in `checklists/`, record issues in `findings/findings-register.csv`, and produce the deliverable using `templates/pentest-report-template.md`. Track fixes in `remediation/remediation-tracker.csv`.

## Legal & Ethical Notice

This material is provided for authorized, lawful security testing and educational purposes only. Unauthorized access to computer systems is illegal. See `scope-rules-of-engagement/` for the authorization requirements that must be met before any testing begins.

## License

Released under the [MIT License](LICENSE).
