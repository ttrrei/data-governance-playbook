# Data Access Control

Data access control ensures that people, systems, and partners can use the data they need while respecting security, privacy, contractual, and ethical constraints.

It is the practical mechanism behind classification (`data-classification.md`): a level like "Confidential" only means something if it translates into who can actually request, approve, and receive access.

## Why It Matters

* Both MVPs treat "unclear access approval" and "informal access decisions" as signals that governance is not yet operational.
* Access that is easy to grant and never reviewed tends to only grow — people accumulate access as they change roles, and it is rarely removed.
* Sensitive and privileged access decisions carry outsized risk relative to how quickly they're often made; a small amount of structure goes a long way.

## Principles

* **Least privilege** — grant the minimum access needed to do the job, not the most convenient amount.
* **Need to know** — a business reason must exist for access to Confidential or Restricted data, not just organizational proximity to it.
* **Role-based where possible** — standard roles reduce one-off, hard-to-track grants.
* **Segregation of duties** — conflicting responsibilities (for example, requesting and approving one's own access) should not sit with the same person.
* **Time-bound for elevated access** — privileged, emergency, and third-party access should expire by default, not persist until someone remembers to remove it.

## Access Request and Approval Workflow

A minimum workflow, independent of tooling:

1. Requester states the business justification and the specific data or system needed.
2. The asset's classification determines who must approve (see below).
3. Access is provisioned and logged.
4. The requester and their manager are notified once access is active.

**Approval by classification:**

| Classification | Minimum approval |
| --- | --- |
| Public / Internal | Manager or system owner |
| Confidential | Data owner |
| Restricted, privileged, or emergency access | Data owner **plus** an approver outside the requester's own reporting chain |

The extra approver for Restricted and privileged access is not bureaucracy for its own sake — it is what keeps someone from being able to grant themselves, or a direct report, sensitive access with no second opinion.

## Review and Revocation

Access is not a one-time decision. See `operating-model/access-review-cadence.md` for how often different levels of access should be re-checked.

Access should also be revoked promptly, not just reviewed periodically, when:

* A person changes roles and no longer needs the previous access.
* A contract, engagement, or employment ends.
* Access was granted for a specific project or investigation that has concluded.
* A periodic review identifies access that is no longer justified.

## Rule of Thumb

Access without a review cadence is a grant, not a control — if nobody ever checks whether access is still needed, it will never be removed.

