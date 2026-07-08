# Implementation Roadmap

A lightweight sequence for taking either MVP from zero to a running operating pattern. This describes sequencing, not a big-bang program — most of the early phases can be done for a single critical asset in days, not months.

## Why It Matters

* Without a sequence, teams often try to do ownership, quality, access, and metrics all at once for every asset, and the effort collapses under its own scope — exactly the "governing everything at once" anti-pattern.
* Jumping straight to metrics before ownership and trust are in place produces KPIs that measure theater, not fact.
* A short, named sequence makes it easier to say "we are at Phase 1 for this domain" instead of leaving progress ambiguous.

## Phases

| Phase | Objective | Uses |
| --- | --- | --- |
| 0. Inventory | Identify a small number of critical data assets and their current gaps. | Critical Data Asset List (or AI Use Case Register) |
| 1. Establish ownership and meaning | Assign a data owner and steward; write approved definitions for disputed terms. | Ownership Register, Business Glossary |
| 2. Make trust and access visible | Classify sensitivity, define quality expectations, set a visible Trust Status, and put an access approval workflow in place. | Data Asset Profile, `concepts/data-classification.md`, `concepts/data-access-control.md` |
| 3. Operate the loop | Run the issue workflow when something breaks, and the access review cadence on schedule. | Issue Log, `access-review-cadence.md` |
| 4. Measure and expand | Report a small set of KPIs, then follow the Expansion Path in the relevant MVP doc to add more assets or domains. | `kpi-library.md`, each MVP's Expansion Path |

## Minimum Practice

* Run all five phases for one critical asset before trying to run Phase 0 across many assets at once — depth on one asset teaches more than breadth across ten.
* It's fine for different assets to be at different phases at the same time. The roadmap describes a path per asset or domain, not a single organization-wide milestone.

## Rule of Thumb

If Phase 4 (metrics) is reached before Phase 2 (visible trust and access) for a given asset, the KPIs will be measuring the appearance of governance, not the reality of it.
