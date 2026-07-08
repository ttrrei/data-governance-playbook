# Data Catalog

A data catalog is an inventory of data assets enriched with metadata that helps people discover, understand, evaluate, request, and reuse data.

At MVP scale, the catalog can be a spreadsheet, a wiki page, or a dedicated tool — the format matters far less than whether the entries are actually maintained.

## Why It Matters

* A catalog answers "does this data exist, and can I use it?" before someone spends a day rebuilding something that already exists.
* "Buying a catalog tool before defining ownership" is the first anti-pattern in this repo's list for a reason: a catalog full of unowned entries just documents the problem instead of solving it.
* For AI use cases especially, an asset needs to be findable *and* have an approved-use answer before it should be treated as a candidate data source.

## Minimum Metadata Per Entry

A catalog entry, even a lightweight one, should be able to answer:

| Question | Field |
| --- | --- |
| What is this? | Name and short business description |
| Who owns it? | Data owner (and steward, if different) |
| Where does it come from? | Source system |
| Can I trust it? | Trust status (green / amber / red) |
| Is it sensitive? | Classification |
| Can I get access? | How to request access, and who approves |

This is deliberately the same information already captured in the Data Asset Profile / AI Data Source Profile — a catalog entry can be generated from that profile rather than maintained as a separate document.

## What a Catalog Does Not Replace

* It does not replace access control — listing a dataset is not the same as being allowed to use it.
* It does not replace quality monitoring — a catalog entry can go stale the day after it's written if nothing keeps the trust status current.
* It does not replace ownership — a catalog entry with no owner is just a very well-organized list of problems.

## Minimum Output

No new artifact is required. Populate catalog entries from the Data Asset Profile / AI Data Source Profile already maintained for critical assets.

## Rule of Thumb

A catalog entry without an owner, a trust status, and a way to request access has documented the data — it has not governed it.

