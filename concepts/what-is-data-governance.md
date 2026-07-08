# What Is Data Governance?

Data governance is the system of decision rights, accountabilities, standards, controls, and operating routines that helps an organization use data responsibly and effectively.

See the README's "What is Data Governance?" section for the full list of what a governance program typically includes (ownership, catalog, glossary, quality, lineage, access control, lifecycle, and operating model). This page focuses on a narrower, frequently misunderstood question: what governance is *not*.

## Why It Matters

* Most governance programs that stall didn't fail on principle — they failed because someone treated a tool purchase, a policy document, or a one-time project as if it were the whole job.
* Knowing what governance is not makes it easier to spot when an initiative has quietly turned into one of these substitutes instead of the real thing.

## What Governance Is Not

| Misconception | Why it's wrong |
| --- | --- |
| "A tool" | A catalog or quality platform can support governance, but buying one does not create ownership or decision rights — see the first anti-pattern in `anti-patterns/common-governance-anti-patterns.md`. |
| "A team that does all the data work" | Governance defines the rules; data management (engineering, platform, operations teams) executes them. Treating governance as an IT-only team is its own anti-pattern. |
| "A policy document" | A published policy that nobody's daily workflow actually follows has produced a document, not governance. |
| "The same as data management" | See the "Governance vs Data Management" distinction in `anti-patterns/common-governance-anti-patterns.md` — confusing the two is one of the most common root causes of governance programs that stall. |
| "A one-time project" | Governance is an operating pattern — the loop in each MVP doc runs continuously, not once. |

## Rule of Thumb

If removing the "governance team" would stop the organization from using data at all, what exists is a data team — not data governance. Governance should still function, even if imperfectly, through named owners and decision rights, when no one central team is doing the work.

