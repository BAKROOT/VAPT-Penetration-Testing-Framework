# Remediation

Tracks the remediation of findings and the retest process that verifies fixes.

## Contents

| File | Purpose |
| --- | --- |
| `remediation-tracker.csv` | Status tracker linking findings to fixes and retests |
| `retest-process.md` | The process for verifying and closing findings |

## Remediation Lifecycle

1. **Assign** — each finding is assigned an owner and a due date based on severity.
2. **Plan** — owner documents the remediation approach.
3. **Implement** — the fix is applied.
4. **Retest** — the tester verifies the fix (see `retest-process.md`).
5. **Close** — verified findings are marked closed; failed retests are reopened.

## Suggested Remediation SLAs

| Severity | Target remediation time |
| --- | --- |
| Critical | 7 days |
| High | 14 days |
| Medium | 30 days |
| Low | 90 days |
| Informational | Best effort / next cycle |

> SLAs are defaults; align them to the client's risk appetite and policy.
