# Rules of Engagement (ROE) — Template

> Complete and obtain signatures BEFORE any testing begins. Replace all `[bracketed]` fields.

## 1. Engagement Overview

- **Client / Organization:** [name]
- **Engagement title:** [name]
- **Assessment type:** [ ] Vulnerability Assessment  [ ] Penetration Test  [ ] Red Team
- **Approach:** [ ] Black box  [ ] Grey box  [ ] White box
- **Engagement ID:** [id]

## 2. Scope

### In-scope targets
| Asset / System | Identifier (IP / URL / range) | Notes |
| --- | --- | --- |
| [asset] | [identifier] | [notes] |

### Out-of-scope (explicitly prohibited)
| Asset / System | Reason |
| --- | --- |
| [asset] | [reason] |

### Permitted techniques
- [ ] Network scanning and enumeration
- [ ] Web/API application testing
- [ ] Authenticated testing (credentials provided)
- [ ] Social engineering — [ ] permitted [ ] not permitted
- [ ] Denial of Service — typically **NOT permitted**
- [ ] Physical testing — [ ] permitted [ ] not permitted

## 3. Testing Window

- **Start date/time:** [datetime, timezone]
- **End date/time:** [datetime, timezone]
- **Allowed hours:** [e.g., business hours only / 24x7]

## 4. Points of Contact

| Role | Name | Contact | Availability |
| --- | --- | --- | --- |
| Client technical POC | [name] | [phone/email] | [hours] |
| Client emergency POC | [name] | [phone/email] | 24x7 |
| Lead tester | [name] | [phone/email] | [hours] |

## 5. Rules & Constraints

- Testing limited strictly to in-scope assets.
- No destructive testing without explicit written approval.
- No exfiltration of real sensitive/personal data; demonstrate access without copying data.
- Source IP addresses for testing: [list].
- Test accounts/artifacts must be removed at the end of the engagement.

## 6. Emergency Procedures (Stop Conditions)

Testing will pause immediately and the emergency POC will be notified if:
- Production instability or outage is observed.
- Evidence of a pre-existing compromise is found.
- Out-of-scope systems or sensitive data are unexpectedly reached.
- The client requests a stop.

## 7. Data Handling

- All engagement data stored on [approved encrypted location].
- Evidence retained for [retention period], then securely destroyed.
- Report delivered via [secure channel].

## 8. Authorization & Sign-off

By signing below, the client confirms they are authorized to permit this testing on the listed assets.

| Party | Name | Title | Signature | Date |
| --- | --- | --- | --- | --- |
| Client authorizing official | | | | |
| Testing lead | | | | |
