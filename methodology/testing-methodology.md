# VAPT Testing Methodology

A phase-by-phase methodology for conducting vulnerability assessments and penetration tests. Each phase lists objectives, key activities, and outputs. All activities are performed strictly within the authorized scope defined in the Rules of Engagement.

## Phase 1 — Pre-engagement & Scoping

**Objective:** Establish authorization, scope, and logistics.

- Confirm signed authorization and Rules of Engagement (ROE).
- Define in-scope targets (IP ranges, domains, applications, accounts).
- Define explicitly out-of-scope systems and prohibited actions.
- Agree on testing windows, points of contact, and escalation paths.
- Confirm data handling, emergency stop conditions, and rules for sensitive data.

**Output:** Approved scope document and signed ROE.

## Phase 2 — Reconnaissance

**Objective:** Gather information about the target.

- **Passive:** OSINT, DNS records, certificate transparency, public repos, search engines.
- **Active:** Host discovery, service banners, technology fingerprinting.
- Build an asset inventory and attack surface map.

**Output:** Target profile and attack surface map.

## Phase 3 — Scanning & Enumeration

**Objective:** Identify live hosts, services, and exposed functionality.

- Port and service scanning.
- Service/version enumeration.
- Web content discovery and application mapping.
- User/role and endpoint enumeration where authorized.

**Output:** Enumerated services and endpoints.

## Phase 4 — Vulnerability Analysis

**Objective:** Identify and validate potential weaknesses.

- Run authenticated and unauthenticated vulnerability checks.
- Manually verify scanner findings to remove false positives.
- Correlate findings with the relevant testing checklist (web/network/API/mobile/cloud).
- Assign a preliminary CVSS v3.1 score to each candidate finding.

**Output:** Validated list of candidate vulnerabilities.

## Phase 5 — Exploitation (Controlled)

**Objective:** Safely demonstrate real-world impact.

- Attempt controlled exploitation to confirm exploitability.
- Avoid destructive actions; coordinate any high-risk tests with the client.
- Capture reproducible evidence (requests, responses, screenshots, commands).
- Respect the emergency stop conditions in the ROE.

**Output:** Confirmed findings with evidence.

## Phase 6 — Post-exploitation & Impact Analysis

**Objective:** Assess the realistic business impact within scope.

- Determine the level of access obtained.
- Assess lateral movement and privilege escalation potential (authorized scope only).
- Document data exposure risk without exfiltrating real sensitive data.
- Clean up any artifacts/test accounts created during testing.

**Output:** Impact narrative and attack path documentation.

## Phase 7 — Reporting

**Objective:** Deliver clear, actionable results.

- Write an executive summary for leadership.
- Document each finding: description, evidence, affected assets, CVSS, risk, remediation.
- Prioritize remediation by risk.
- Use `templates/pentest-report-template.md`.

**Output:** Final assessment report.

## Phase 8 — Remediation & Retest

**Objective:** Verify that issues are fixed.

- Track remediation in `remediation/remediation-tracker.csv`.
- Retest each fixed finding and record verification status.
- Issue a retest summary or updated report.

**Output:** Retest results and closed findings.

## Documentation & Evidence Standards

- Every finding must be reproducible from the documented steps.
- Evidence must be sanitized of unrelated sensitive data before storage.
- Never commit raw evidence or real client data to this repository.
