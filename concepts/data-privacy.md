# Data Privacy

Data privacy governs how personal data is collected, used, shared, retained, and deleted, and what rights the people it describes have over it.

It is distinct from data classification: classification protects data based on business sensitivity, while privacy protects data because it relates to a specific, identifiable person. A dataset can be Confidential and also personal data at the same time — both concepts apply.

## Why It Matters

* Personal data mishandling creates legal, regulatory, contractual, and reputational risk that is usually harder to reverse than a quality issue.
* AI use cases in particular tend to pull personal data into new contexts (training, embeddings, prompts) that the original collection never anticipated.
* Treating privacy as "a Legal problem" instead of a data governance concern is one of the most common ways organizations get surprised by it — see the anti-patterns list.

## Key Terms

| Term | Definition |
| --- | --- |
| Personal data | Any information relating to an identified or identifiable individual. |
| Data subject | The individual the personal data is about. |
| Controller | The organization that decides why and how personal data is processed. |
| Processor | A third party that processes personal data on the controller's behalf and instructions. |
| Processing | Any operation performed on personal data: collecting, storing, using, sharing, or deleting it. |

## Core Principles

Personal data should be:

1. **Collected and used lawfully, fairly, and transparently** — people should not be surprised by how their data is used.
2. **Collected for a specific purpose** — and not reused for a materially different purpose without checking whether that reuse is still appropriate.
3. **Limited to what is necessary** — collect what the purpose requires, not everything that is technically available.
4. **Kept accurate** — inaccurate personal data should be correctable.
5. **Retained no longer than necessary** — see `data-lifecycle.md` for retention and disposal.
6. **Secured appropriately** — classification and access control (see `data-classification.md` and `data-access-control.md`) are how this principle gets implemented in practice.
7. **Accountable** — someone must be able to explain, for any personal data in scope, why it is being used and on what basis.

## Individual Rights

Depending on applicable law and contract, individuals may have the right to:

* Be informed about how their data is used.
* Access a copy of the personal data held about them.
* Request correction of inaccurate data.
* Request deletion, subject to legal or contractual retention obligations.
* Object to certain uses, including marketing.
* Receive their data in a portable format.

This MVP does not define jurisdiction-specific procedures for handling these requests — that belongs to the organization's legal/privacy function. What governance is responsible for is knowing *which datasets contain personal data* well enough that a request can actually be fulfilled when one arrives.

## Additional Review Triggers

Some uses of personal data deserve a second look even when the original collection was fine:

* **Using personal data to train or fine-tune an AI model** — the data may end up represented in ways the original data subject never agreed to.
* **Reusing personal data in a new context** — for example, moving support-ticket data into a churn-prediction model, or product-usage data into a sales-targeting tool.
* **Combining datasets** that individually look low-risk but together become identifying or sensitive.

## Minimum Output

No new artifact is required. Add two fields to the existing Data Asset Profile / AI Data Source Profile:

| Field | Description |
| --- | --- |
| Contains personal data | Yes or no |
| Basis for use | The lawful, regulatory, or contractual basis for processing this personal data |

## Rule of Thumb

If nobody can state the lawful, regulatory, or contractual basis for using a piece of personal data, it is not ready to be used — and that includes using it as AI training or context data.
