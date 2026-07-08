# Data Lifecycle

Data lifecycle management defines what should happen to a data asset from the moment it is created until it is disposed of, so that retention and disposal are deliberate decisions rather than defaults nobody chose.

## Why It Matters

* "We'll keep it forever, just in case" is not a retention decision — it is the absence of one, and it quietly increases privacy, security, and storage risk over time.
* Legal, regulatory, and contractual obligations often set a *minimum* retention period; storage cost and privacy risk argue for a *maximum* one. Both need to be known.
* Disposal is the stage every stub-level governance program forgets. An asset with an owner, a glossary entry, and a trust status but no disposal plan is only half governed.

## Lifecycle Stages

| Stage | What should be true |
| --- | --- |
| Create / capture | Data is captured from an approved source using an agreed definition. |
| Process / transform | Any transformation logic is documented well enough to explain how a downstream value was derived. |
| Store | Data is stored in a system consistent with its classification (see `data-classification.md`). |
| Use | Data is used only for purposes consistent with its approved usage and, if personal, its stated basis for use (see `data-privacy.md`). |
| Share | Internal or external sharing follows the access and classification rules for that asset. |
| Archive | Inactive data that still needs to be retained is moved to lower-cost, still-controlled storage. |
| Dispose | Data is deleted, anonymized, aggregated, or destroyed once its retention period ends. |

## Retention and Disposal

Set retention at the level of a data **category or asset**, not record by record — a rule like "customer support tickets: retain 3 years after case closure" is maintainable; a rule that has to be evaluated per record is not, unless a specific record has an exception.

Disposal is not always "delete." Depending on the asset and its future value, the right disposal method may be:

* **Delete** — remove the data entirely.
* **Anonymize** — strip identifying attributes so what remains is no longer personal data.
* **Aggregate** — collapse individual records into summary statistics and discard the underlying detail.
* **Destroy** — for physical media or hard copies, certified physical destruction.

**Legal hold** overrides normal retention and disposal: if data is or may become relevant to litigation, investigation, or audit, its scheduled disposal must be suspended until the hold is lifted, regardless of what the retention schedule says.

## Minimum Output

No new artifact is required. Add two fields to the existing Data Asset Profile / AI Data Source Profile:

| Field | Description |
| --- | --- |
| Retention period | How long this asset (or category) is kept, and from what trigger date |
| Disposal method | Delete, anonymize, aggregate, or destroy |

## Rule of Thumb

If nobody can say how long a data asset should be kept, the real answer is "forever" — and forever is a retention decision too, it just hasn't been made on purpose.
