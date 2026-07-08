# Reconciliation and Recovery

Reconciliation confirms that two representations of the same data actually agree with each other. Recovery is what happens when they don't, and the mismatch can't be explained away.

## Why It Matters

* A Trust Status of "Green" that has never been checked against its source is an unverified claim, not a fact.
* Small, unexplained differences between a report and its source are one of the quietest ways trust erodes — nobody declares an incident, people just start double-checking the numbers themselves.
* Recovery only works well under pressure if it was thought through before the pressure showed up.

## When to Reconcile

| Type | What's being compared |
| --- | --- |
| Source-to-copy | Does a downstream copy of the data match its source (counts, key values)? |
| Copy-to-report | Does a report or metric match the underlying data it was built from? |
| Cross-system | Do two systems that are both expected to reflect the same reality actually agree? |
| Point-in-time | After a fix, migration, or backfill, does the data match a known-good snapshot? |

## Minimum Reconciliation Practice

For each critical data asset, know:

* What it should match, and against what source.
* How often that check should run.
* What counts as "a match" — exact agreement, or within an explicitly stated tolerance.

An unexplained difference becomes an entry in the Issue Log (`issue-management.md`) — it does not get quietly waved off as "probably a timing thing."

## Recovery Steps

When data is found missing, duplicated, corrupted, or inconsistent:

1. Classify severity and downstream impact, using the severity guide in `issue-management.md`.
2. Pause downstream publication if continuing to use the data would spread the problem further.
3. Identify the last known-good state to restore from.
4. Restore or reconstruct the data.
5. Reconcile the restored data against the known-good state and a sample of records.
6. Document the root cause as an issue, following the workflow in `mvps/general-enterprise-mvp.md` §11.
7. Get the data owner's sign-off that trust is restored before closing the incident.

## Minimum Output

No new artifact is required. Log reconciliation discrepancies and recovery events through the existing Issue Log.

## Rule of Thumb

If the first time a recovery process is used is during a real incident, it was never actually tested.
