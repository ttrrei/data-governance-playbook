# Business Glossary

A business glossary defines the terms, metrics, classifications, and business concepts that teams use when discussing and interpreting data.

Its job is narrow but important: make sure that when two people say "active customer" or "net revenue," they mean the same thing.

## Why It Matters

* Inconsistent definitions are one of the most common reasons business users stop trusting reports — the data isn't necessarily wrong, the definitions just disagree.
* A glossary that tries to define every column in every table becomes unmaintained within a quarter. A glossary that defines the terms people actually argue about gets used.
* For metrics, the calculation logic is the part that actually causes disagreement — the definition alone is rarely enough.

## What Belongs in the Glossary

Start with terms that are frequently used, frequently disputed, or tied directly to a business decision — see the example list in `mvps/general-enterprise-mvp.md` (customer, revenue, churn, conversion rate, and similar). Do not start by trying to define every field in every table; that is a data dictionary exercise, not a glossary exercise, and it belongs at the technical metadata layer, not here.

## Anatomy of a Good Entry

A useful glossary entry, whether tracked in a spreadsheet or `templates/glossary-template.md`, includes:

* The approved definition, in plain business language.
* An owner who can arbitrate disputes about the definition.
* Calculation logic, if the term is a metric — this is usually where the real disagreement lives.
* Approved usage, and any known exceptions or edge cases.
* Synonyms and deprecated terms, so old names don't quietly resurface with a different meaning.

## Minimum Output

Use the lightweight glossary table already defined in the MVP docs (term, definition, owner, calculation logic, approved usage), or `templates/glossary-template.md` for a fuller version once a term needs more history and approval tracking.

## Rule of Thumb

A critical metric should have one approved definition, one owner, and one preferred usage — if two teams can each produce a different number for the same metric name, the glossary has a gap, not the teams.

