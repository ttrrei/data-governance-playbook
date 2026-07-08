# Data Lineage

Data lineage describes where data comes from, how it changes, and where it is consumed.

## Why It Matters

* When a source system or pipeline changes, lineage is what tells you which reports, metrics, or AI use cases are affected — without it, that only gets discovered when something downstream breaks.
* Full technical, field-level lineage is expensive to build and maintain. Most of the MVP's value comes from a much cheaper version: business lineage.
* For AI use cases, lineage also has to answer a version question that traditional BI lineage usually doesn't: which snapshot of the data produced this specific output.

## Business Lineage vs. Technical Lineage

| | Business lineage | Technical lineage |
| --- | --- | --- |
| Answers | Which source feeds this report or metric, and who is affected if it changes? | Exactly which job, query, or transformation step produced this field? |
| Cost to maintain | Low — a short list per critical asset | High — requires pipeline-level tooling or metadata capture |
| MVP priority | Start here | Add later, as the expansion path in each MVP doc describes |

Start with business lineage for every critical data asset. Technical, field-level lineage is valuable but is explicitly out of scope for this MVP — see "What This MVP Covers" in `mvps/general-enterprise-mvp.md`.

## Minimum Lineage Questions

For each critical asset, lineage should be able to answer:

1. Which source(s) does this asset come from?
2. What happens to the data between the source and this asset (in plain terms, not full transformation logic)?
3. Who or what consumes this asset downstream, and would be affected if it changed?

For AI use cases, add a fourth question: which version or snapshot of the data was used — see "AI Data Usage, Lineage, and Version" in `mvps/ai-ready-mvp.md`.

## Minimum Output

Use `templates/data-lineage-template.md` (upstream sources, transformations, downstream consumers) for critical assets. For AI use cases, use the AI Data Lineage Map already defined in the AI-Ready MVP instead, since it also captures version and snapshot information that business lineage alone does not.

## Rule of Thumb

If nobody can say what breaks downstream when a source changes, there is no lineage — only hope.

