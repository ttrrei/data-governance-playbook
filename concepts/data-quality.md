# Data Quality

Data quality describes whether data is fit for its intended business, analytical, operational, or AI use.

It is the substance behind the Trust Status field both MVPs use (green / amber / red). A Trust Status is only credible if there is a shared understanding of what "quality" was actually checked to produce it.

## Why It Matters

* "Trust Status: Green" means nothing if two people would disagree about what was checked to get there.
* Not every quality dimension matters equally for every use case — checking the wrong ones wastes effort and still misses the problem that actually breaks trust.
* Quality issues found by a customer or an executive are more expensive than the same issue found by a scheduled check.

## Quality Dimensions

| Dimension | Definition | How it's typically checked |
| --- | --- | --- |
| Accuracy | The data correctly reflects the real-world value or source of truth. | Compare against the authoritative source or a known-correct reference. |
| Completeness | Required fields and records are present. | Non-null checks, expected record counts. |
| Timeliness | Data is available within the time window consumers need. | Freshness or latency checks against an SLA. |
| Consistency | The same value agrees across systems and reports. | Cross-system comparison. |
| Validity | Values conform to expected formats, ranges, or reference lists. | Format and range validation. |
| Uniqueness | Records are not unintentionally duplicated. | Duplicate detection on key fields. |
| Integrity | Relationships between records remain valid. | Referential checks (for example, a transaction pointing to a real customer). |

## Dimension Priority by Use Case

Not every use case needs all seven dimensions checked with equal rigor. As a starting heuristic:

| Use case | Dimensions to prioritize first |
| --- | --- |
| Executive reporting and KPIs | Accuracy, consistency, timeliness |
| Operational decisions | Completeness, timeliness, validity |
| AI training or RAG context | Accuracy, completeness, integrity |

## Minimum Output

No new artifact is required. When filling in the Quality Expectations field of the Data Asset Profile / AI Data Source Profile, name the specific dimension(s) and check(s) behind that expectation — for example, "Completeness: customer ID must not be null" rather than just "data should be complete."

## Rule of Thumb

A Trust Status without a named dimension behind it is an opinion, not a quality check.

