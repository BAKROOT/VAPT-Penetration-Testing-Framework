# Scope Definition — Template

> Defines exactly what is and is not included in the engagement. Attach to the ROE. Replace all `[bracketed]` fields.

## Engagement

- **Client:** [name]
- **Engagement ID:** [id]
- **Assessment type:** [VA / PT / Red Team]
- **Test perspective:** [External / Internal / Both]
- **Knowledge level:** [Black / Grey / White box]

## In-Scope Assets

| # | Asset name | Type (web/API/host/network/mobile/cloud) | Identifier (URL / IP / range / app) | Environment (prod/staging) | Notes |
| --- | --- | --- | --- | --- | --- |
| 1 | [name] | [type] | [identifier] | [env] | [notes] |
| 2 | | | | | |

## Out-of-Scope Assets

| # | Asset / System | Identifier | Reason |
| --- | --- | --- | --- |
| 1 | [name] | [identifier] | [reason] |

## Credentials Provided (Grey/White box)

| Role | Username | Provided via | Notes |
| --- | --- | --- | --- |
| [role] | [user] | [secure channel] | Do not store real credentials in this repo |

## Constraints & Exclusions

- Prohibited techniques: [e.g., DoS, social engineering, physical].
- Rate limiting / throttling requirements: [details].
- Maintenance windows to avoid: [details].
- Third-party / hosted assets requiring separate authorization: [list].

## Source IPs / Testing Infrastructure

- Tester source IP(s): [list]
- User-Agent / identifier for test traffic: [value]

## Success Criteria & Objectives

- [e.g., identify exploitable vulnerabilities in the customer portal]
- [e.g., assess whether an external attacker can reach internal systems]

## Approvals

| Role | Name | Signature | Date |
| --- | --- | --- | --- |
| Client owner | | | |
| Testing lead | | | |
