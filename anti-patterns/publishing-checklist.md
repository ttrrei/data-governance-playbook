# Publishing Checklist

A short checklist for anyone adapting internal governance content — like this repository itself — for external or open-source publication.

## Why It Matters

* This repository's own history includes a pass where content was expanded and then deliberately stripped back down, likely for exactly this reason. Company- and industry-specific detail creeps into drafts easily and needs a deliberate check before it goes out the door.
* A document can pass a "remove the company name" pass and still only make sense to people who work at that company — sanitization and generalization are different bars, and both need to be checked.
* It is easier to catch this before publication than after.

## Confidentiality Sanitization

* No company, product, team, or internal project names.
* No internal links, ticket references, file paths, or tool names — replace with generic placeholders if a concrete example is needed.
* No real people, customer names, account identifiers, or other production examples.
* No production thresholds, SLAs, or figures that would reveal internal strategy, risk posture, or performance.

## Security Sanitization

* No credentials, keys, network details, or specific security control implementations.
* No named vendors or tools, unless keeping one as a deliberate, disclosure-approved example.

## Generalization Review

Sanitized is not the same as generalized. A passage can have every company name removed and still only be usable by one industry or one specific process.

* Check whether each example still generalizes across industries and company sizes, not just across teams within the same company.
* Watch for content that is technically anonymous but still structurally specific to one business model (a particular regulatory regime, a particular kind of transaction, a particular org chart).

## Usability Review

* A reader from a different organization should be able to follow the document without needing it translated for their context.
* Terminology should be internally consistent with the rest of the document set (for this repository: role names in `operating-model/roles-and-responsibilities.md`, Trust Status terminology, and so on).

## After Publication

* Identify the published version as the source of truth going forward — do not let a private working draft silently diverge from what was actually published.
* Periodically re-check published content for drift: internal assumptions that crept back in during a later edit, or terminology that quietly stopped matching the rest of the document set.

## Rule of Thumb

If a reader from a different organization, industry, and jurisdiction can pick up the published document and immediately understand what to do next, sanitization is probably complete. If they would need to ask what a term means "at your company" first, it isn't.
