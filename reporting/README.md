# Reporting Standards

Defines how engagement deliverables are produced, what evidence standards apply, and the quality checks performed before delivery.

## Deliverables

| Deliverable | Source template |
| --- | --- |
| Full technical report | `templates/pentest-report-template.md` |
| Executive summary | `templates/executive-summary-template.md` |
| Per-finding write-ups | `templates/finding-writeup-template.md` |
| Retest summary | Produced after retest (see `remediation/retest-process.md`) |

## Report Quality Checklist

- [ ] Executive summary is non-technical and accurate.
- [ ] Every finding has severity, CVSS v3.1 score, and vector string.
- [ ] Every finding includes reproducible steps and sanitized evidence.
- [ ] Remediation guidance is specific and actionable.
- [ ] Scope and limitations are clearly stated.
- [ ] No real credentials, secrets, or unrelated sensitive data are included.
- [ ] Severity ratings are consistent with the CVSS scoring guide.
- [ ] Report is peer-reviewed before delivery.

## Evidence Handling

- Sanitize evidence to remove unrelated sensitive data.
- Reference evidence by ID; store raw evidence in an approved, access-controlled location (never in this repository).
- Retain evidence per the agreed retention period, then securely destroy it.

## Delivery

- Deliver reports via a secure, encrypted channel agreed in the ROE.
- Mark all deliverables with the appropriate confidentiality classification.

## Classification

All engagement reports are **CONFIDENTIAL** by default unless the client specifies otherwise.
