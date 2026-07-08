# Evidence and Audit Readiness

Evidence and audit readiness means being able to show, after the fact, that a governance activity actually happened — not just that it's described somewhere as a process.

## Why It Matters

* Governance that only exists in people's memory doesn't survive a personnel change, an audit, or a dispute about what was decided and when.
* "Prove it happened" is one of the most common ways a governance program that looks fine on paper turns out to be weaker in practice.
* Retaining evidence as a byproduct of doing the work is far cheaper than reconstructing it after the fact.

## What Evidence Should Exist, By Control Area

This is not a new artifact to maintain — it's a reminder that the artifacts already defined elsewhere in this repo *are* the evidence, as long as they're kept up to date rather than overwritten in place.

| Control area | Evidence that should exist | Where it already lives |
| --- | --- | --- |
| Ownership | Who was assigned as owner, and when | Ownership Register |
| Business definitions | The approved definition, its owner, and when it was approved | Business Glossary |
| Classification and privacy | The assigned classification and, if personal data, the basis for use | Data Asset Profile / AI Data Source Profile |
| Data quality | What was checked, and the result of the last check | Data Asset Profile, `concepts/data-quality.md` |
| Access control | Who requested, who approved, and the last review date and outcome | `templates/access-request-template.md`, `access-review-cadence.md` |
| Issue management | What went wrong, who owned it, and confirmation that trust was restored | Issue Log, `templates/data-issue-template.md` |
| Reconciliation and recovery | What was compared, what didn't match, and how it was resolved | `reconciliation-and-recovery.md` |

## Minimum Practice

* Don't overwrite a status field in place without keeping the prior value — a Trust Status that silently changed from Red to Green with no record of when or why is not evidence, it's just the current state.
* Apply the retention period from `concepts/data-lifecycle.md` to governance records themselves, not just to the underlying data.
* If a reviewer, auditor, or new team member couldn't reconstruct "what happened and when" from these artifacts alone, the evidence isn't there yet, regardless of what actually happened.

## Rule of Thumb

If the only proof a governance activity happened is someone's memory, it didn't happen for audit purposes.
