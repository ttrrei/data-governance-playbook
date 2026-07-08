# Data Ownership

Data ownership assigns accountability for data meaning, quality expectations, access decisions, lifecycle rules, and issue resolution.

Ownership is accountability, not day-to-day execution. The three roles that split this work are already defined in `operating-model/roles-and-responsibilities.md`: the **Data owner** is accountable, the **Data steward** does the day-to-day definition and quality work, and the **Technical custodian** runs the underlying platform. For a worked example of how to anchor ownership to a business function (revenue, customer, product, and so on), see the Ownership section of `mvps/general-enterprise-mvp.md`.

## Why It Matters

* An asset with no named owner has no one who can approve a definition, resolve a dispute, or decide an access exception — it just accumulates informal, inconsistent answers instead.
* Ownership assigned to whoever happens to be technically closest to the data (often a data engineer) tends to produce technically correct but business-meaningless definitions.
* Ownership without real decision authority is not ownership — see `operating-model/decision-rights.md`.

## Common Ownership Pitfalls

* **Assigned by proximity, not accountability.** Being able to query the data is not the same as being accountable for what it means.
* **No time allocated.** A steward named in a spreadsheet but given no capacity to actually maintain definitions or triage issues is an owner in name only.
* **Split across too many people.** If a domain has three "co-owners" with no clear tiebreaker, decisions stall — see `templates/data-domain-template.md` for how to scope a domain so one owner can reasonably cover it.
* **Owner is never told when something breaks.** Ownership without a working issue path (`operating-model/issue-management.md`) is accountability with no way to act on it.

## Minimum Output

Use the Ownership Register already defined in the MVP docs (asset, data owner, data steward, technical owner, related KPI or process). This concept does not introduce a separate artifact.

## Rule of Thumb

If the named owner cannot explain what the data means or who depends on it, ownership exists on paper only.

