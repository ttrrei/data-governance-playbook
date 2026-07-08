# Data Classification

Data classification assigns a sensitivity level to a data asset so that handling, sharing, and access decisions can be made consistently instead of case by case.

It is the missing definition behind a field both MVPs already use: every Data Asset Profile and AI Data Source Profile asks for a "Sensitivity: public, internal, confidential, or restricted" value. This concept defines what those four words actually mean and how to assign them.

## Why It Matters

* Without a shared definition, "confidential" means something different to every team that types it into a profile.
* Access approval, external sharing, and AI usage decisions all depend on classification being assigned consistently, not guessed at.
* A classification level should be assignable in minutes from a short table, not from a legal review — that is what keeps it usable at MVP scale.

## Classification Levels

| Level | Definition | Typical examples |
| --- | --- | --- |
| Public | Approved for unrestricted external release. No harm from disclosure. | Published marketing content, public product pages, already-released reports. |
| Internal | Intended for use inside the organization. Limited harm if it leaked externally, but not meant to be shared freely. | Internal procedures, working documents, non-sensitive operational metrics. |
| Confidential | Disclosure could cause real business, customer, or competitive harm. | Customer records, financial reports before release, contracts, most business-critical datasets. |
| Restricted | Disclosure could cause severe harm: regulatory, financial, safety, or reputational. | Authentication secrets, highly sensitive personal data, material non-public information. |

## Minimum Handling Expectations

| Control | Restricted | Confidential | Internal | Public |
| --- | --- | --- | --- | --- |
| Access | Named individuals only, approved by the data owner | Role-based, approved by the data owner | Any employee or contractor with a business need | Anyone |
| External sharing | Not permitted without explicit data owner and risk partner approval | Requires data owner approval and a contractual or legal basis | Generally avoided; case-by-case | Freely shareable once approved for publication |
| Disposal | Secure deletion or destruction, evidenced | Secure deletion | Standard deletion | No special requirement |

Treat this as a floor, not a ceiling. A domain can apply stricter handling than its classification requires; it should never apply looser handling.

## Default Classification by Data Type

| Data type | Typical default | Notes |
| --- | --- | --- |
| Personal or customer-identifying data | Confidential or Restricted | Depends on sensitivity of the specific fields — see `data-privacy.md`. |
| Financial results before public release | Restricted | Downgrades to Public only after formal release. |
| Authentication credentials, keys, secrets | Restricted | Never Internal or lower, regardless of context. |
| Internal operating metrics and working documents | Internal | Default for most day-to-day business documents. |
| Approved external communications | Public | Only after going through the organization's normal publication approval — being "already written" is not the same as being approved for release. |

## Minimum Output

No new artifact is required. Record the classification level directly in the **Sensitivity** field of the Data Asset Profile (General Enterprise MVP) or the AI Data Source Profile (AI-Ready MVP) that already exists for each critical asset. Adding a sixth artifact just to track classification would be heavier than the problem requires.

## Rule of Thumb

If a data owner is unsure which level applies, assign the higher one until it is confirmed otherwise — and never let something become "Public" simply because it hasn't been marked as anything else yet.
