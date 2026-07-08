# Access Review Cadence

Granting access is a decision at a point in time. A review cadence is what checks whether that decision is still correct later — most access, left unreviewed, only grows.

## Why It Matters

* People accumulate access as they change roles; almost nobody proactively asks to have old access removed.
* A review that happens on paper but never actually removes anything is not a control, it's a scheduled formality.
* Restricted and privileged access carry enough risk that they need a materially tighter cadence than everyday access.

## Review Schedule

| Access type | Review frequency | Reviewer |
| --- | --- | --- |
| Standard (Public / Internal data) | Annually | Manager or system owner |
| Confidential data | Semi-annually | Data owner |
| Restricted or privileged access | Monthly, or immediately after each use for emergency access | Data owner plus an approver outside the requester's chain |
| Third-party or contractor access | At each contract milestone, and at minimum quarterly | Business sponsor |
| Dormant accounts (no activity for an extended period) | Quarterly | Data owner or technical custodian |

Event-driven reviews (role change, contract end, termination) should happen immediately and are not a substitute for the scheduled cadence above — they cover the gap between reviews, not replace them.

## Common Failure Modes

| Failure mode | What it looks like |
| --- | --- |
| Rubber-stamp review | The reviewer clicks "approve all" without checking whether each grant is still justified. |
| Review without removal | The review happens on schedule, but access is never actually revoked as a result. |
| No independent reviewer for sensitive access | The same person who approved the original grant is the only one reviewing it later. |
| Leavers caught late | A departed employee's access is only found and removed at the next scheduled review, not at departure. |
| No evidence retained | Nobody can show, after the fact, that a review happened or what was decided. |
| Reviewer fatigue | The same person reviews the same list so many times that it becomes a formality rather than a real check. |

## Minimum Output

No new artifact is required. Record the last review date and reviewer directly against the access approvals already captured through `templates/access-request-template.md`.

## Rule of Thumb

If a review cycle finishes without anyone's access being removed, either the organization has reached perfect least privilege, or the review is not doing real work. The second explanation is almost always the correct one.
