# RACI for the Minimum Artifacts

This intentionally covers only the five minimum artifacts already defined in the MVP docs — it is not a comprehensive activity-by-activity RACI. For decision-level accountability beyond artifact maintenance (who decides a business definition, an access exception, and so on), see `decision-rights.md`.

## Roles

Using the roles already defined in `roles-and-responsibilities.md`: Executive sponsor (ES), Data governance lead (DGL), Data owner (DO), Data steward (DS), Technical custodian (TC), Risk/privacy/security partner (RPS), Data consumer (DC).

## RACI

| Artifact | ES | DGL | DO | DS | TC | RPS | DC |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Critical Data Asset List | I | A | R | C | I | C | I |
| Ownership Register | I | A | R | C | I | I | I |
| Business Glossary | I | I | A | R | I | C | C |
| Data Asset Profile (trust status, quality) | I | I | A | R | C | C | I |
| Issue Log | I | I | A | R | C | C | R* |

\* Data consumers are Responsible for reporting issues into the log; the Data steward is Responsible for triaging and maintaining it.

## Design Notes

* The Executive sponsor and Risk/privacy/security partner are Consulted or Informed here, not Accountable — if either becomes Accountable for routine artifact upkeep, accountability has likely been re-centralized away from the domain, which works against the "start small, keep it close to the business" principle both MVPs rely on.
* The Data governance lead is Accountable only for the Critical Data Asset List and Ownership Register — the operating-model-level artifacts — not for domain-specific content like glossary definitions or trust status, which stay with the Data owner.

## Rule of Thumb

If the same person shows up as both Accountable and Responsible on every row, ownership and execution haven't actually been separated — that's a sign the "steward" role exists on paper only.
