# Retest Process

After the client remediates findings, a retest verifies that fixes are effective and that no regressions were introduced.

## When to Retest

- After the client confirms a finding has been remediated, or
- At an agreed milestone (e.g., 30 days after report delivery).

## Retest Scope

- Limited to findings marked as remediated in `remediation-tracker.csv`.
- Same authorization and ROE rules apply; confirm the testing window.

## Retest Steps

1. Reproduce the original finding using the documented steps from the finding write-up.
2. Confirm whether the issue is still exploitable.
3. Check for incomplete fixes or new variants introduced by the change.
4. Record the result: **Pass** (fixed), **Fail** (still present), or **Partial** (partially fixed).
5. Update `remediation-tracker.csv` with the retest result and date.

## Outcomes

| Result | Action |
| --- | --- |
| Pass | Mark finding Closed. |
| Fail | Reopen finding; notify owner with details. |
| Partial | Keep open; document what remains. |

## Retest Deliverable

Produce a short retest summary that lists each retested finding, its original severity, and the verification result. For larger engagements, issue an updated report appendix reflecting the new status.

## Evidence

Capture sanitized evidence demonstrating the fix (or its absence). Do not store real sensitive data in this repository.
