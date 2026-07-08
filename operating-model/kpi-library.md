# KPI Library

Both MVP docs define qualitative "Success Signals" for knowing the MVP is working. This library gives a small set of numbers to go with them — enough to track trend over time, not a full metrics program.

## Why It Matters

* "Users trust the data more" is a real signal but hard to track quarter over quarter. A handful of numbers make the trend visible.
* A KPI library that tries to cover everything becomes its own maintenance burden — see "Measuring governance by documentation volume" in the anti-patterns list. The point is a small, honest set, not a comprehensive one.
* KPIs should be reported somewhere real (a governance forum), or they are not really being used.

## Starter Set

Pick from this set rather than building a longer one. Most MVPs should be able to report all of these from the artifacts they already maintain.

| KPI | What it measures | Source |
| --- | --- | --- |
| Ownership coverage | % of critical data assets with a named data owner | Ownership Register |
| Trust status currency | % of critical assets with a trust status reviewed in the last quarter | Data Asset Profile |
| Glossary coverage | % of frequently-used or disputed terms with an approved definition | Business Glossary |
| Mean time to resolve | Average time from issue logged to issue closed | Issue Log |
| Issue recurrence rate | % of closed issues that reopen or recur | Issue Log |
| Access review completion | % of scheduled access reviews completed on time | `access-review-cadence.md` |

For the AI-Ready MVP, add:

| KPI | What it measures | Source |
| --- | --- | --- |
| Approved source coverage | % of AI use cases using only approved data sources | AI Use Case Register / Approved AI Data Source List |

## Additional KPIs (Optional)

Add these only once the starter set is established and reported consistently. They are not a checklist to complete:

* Data quality score, broken down by dimension (see `concepts/data-quality.md`).
* Orphaned account count (accounts with no valid owner or active employment/contract status).
* Catalog or glossary adoption (active use, not just entry count).
* Recurring-issue count by root-cause category.
* Stakeholder satisfaction with governance processes.

## KPI Definition Template

When defining any KPI, capture:

* **Name** and what it measures.
* **Formula or method.**
* **Data source.**
* **Reporting frequency.**
* **Owner** (who is accountable for the number being right and current).

## Minimum Output

Start with 3-5 KPIs from the starter set — not all six or seven at once — and report them at the governance forum cadence already defined in `governance-forum.md`.

## Rule of Thumb

A KPI that nobody reports at a governance forum is a number, not a metric. And more KPIs is not the goal — the goal, as the MVP docs already say, is trust, clarity, and accountability, not documentation volume.
