## Governance vs Data Management

Before discussing anti-patterns, it is useful to distinguish data governance from data management.

| Concept         | Focus                                                                                      | Example Questions                                                                                                            |
| --------------- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| Data Governance | Defines decision rights, accountability, policies, standards, and control mechanisms.      | Who owns this data? What quality standard applies? Who can approve access? Which data assets are certified?                  |
| Data Management | Executes the operational activities required to manage data according to governance rules. | How is the data pipeline maintained? How are quality checks implemented? How is metadata updated? How is access provisioned? |

In simple terms:

* Governance defines the rules, ownership, and accountability.
* Management executes the rules through processes, systems, and daily operations.

Many governance failures happen when organizations confuse these two concepts. For example, implementing a catalog tool is data management activity; deciding who owns metadata quality and how certification works is data governance.

---

## Warning Signs to Add to Each Anti-pattern

### 1. Buying a Tool Before Defining Ownership

#### Warning Signs

You may be falling into this anti-pattern if you hear statements like:

* "Once we buy the catalog tool, our data assets will become clear."
* "The platform will tell us who owns the data."
* "We can define ownership after the tool is implemented."

---

### 2. Trying to Govern Everything at Once

#### Warning Signs

You may be falling into this anti-pattern if you hear statements like:

* "We need to catalog all enterprise data before showing value."
* "Governance is not useful unless it covers every system."
* "Let’s define standards for all data domains in phase one."

---

### 3. Treating Governance as an IT-only Initiative

#### Warning Signs

You may be falling into this anti-pattern if you hear statements like:

* "The data platform team should own governance."
* "Business teams only need to consume the governed data."
* "Metric definitions can be handled by the data team."

---

### 4. Creating Policies Without Operational Workflows

#### Warning Signs

You may be falling into this anti-pattern if you hear statements like:

* "We have already published the policy, so governance is in place."
* "Teams should just follow the standard."
* "The process details can be worked out later."

---

### 5. Measuring Governance by Documentation Volume

#### Warning Signs

You may be falling into this anti-pattern if you hear statements like:

* "We documented 500 tables this quarter, so governance is progressing well."
* "The goal is to maximize glossary coverage."
* "Success means every column has a description."

---

### 6. Building a Governance Council Without Decision Rights

#### Warning Signs

You may be falling into this anti-pattern if you hear statements like:

* "The council can discuss the issue, but the final decision sits elsewhere."
* "We meet every month, but unresolved ownership conflicts keep coming back."
* "The council is mainly for alignment."

---

### 7. Applying the Same Governance Model to All Data

#### Warning Signs

You may be falling into this anti-pattern if you hear statements like:

* "Every dataset should go through the same governance process."
* "All data assets need the same level of documentation and approval."
* "A single governance workflow will keep things simple."

---

### 8. Ignoring AI-specific Data Risks

#### Warning Signs

You may be falling into this anti-pattern if you hear statements like:

* "If the data is good enough for dashboards, it is good enough for AI."
* "The AI team can decide which data sources to use."
* "RAG only retrieves existing documents, so it does not need additional governance."

---

## Anti-pattern Relationship Matrix

Some anti-patterns are not isolated. One weak governance practice often creates or amplifies another.

| Source Anti-pattern                             | Often Leads To                                        | Why They Are Connected                                                                                                                                    |
| ----------------------------------------------- | ----------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Buying a tool before defining ownership         | Measuring governance by documentation volume          | Tool-first programs often measure success by metadata quantity instead of accountability and adoption.                                                    |
| Buying a tool before defining ownership         | Creating policies without operational workflows       | Tools may expose metadata gaps, but they do not define how governance decisions are made or enforced.                                                     |
| Trying to govern everything at once             | Measuring governance by documentation volume          | Broad scope encourages teams to count documented assets instead of solving high-value business problems.                                                  |
| Treating governance as an IT-only initiative    | Building a governance council without decision rights | If business accountability is missing, governance forums often become discussion groups rather than decision-making bodies.                               |
| Treating governance as an IT-only initiative    | Creating policies without operational workflows       | IT-led governance may produce standards that are not embedded into business processes.                                                                    |
| Creating policies without operational workflows | Measuring governance by documentation volume          | When execution is weak, teams often rely on policy documents and artifacts as evidence of progress.                                                       |
| Applying the same governance model to all data  | Trying to govern everything at once                   | A uniform model usually expands scope too broadly and makes governance too heavy.                                                                         |
| Ignoring AI-specific data risks                 | Applying the same governance model to all data        | Treating AI data usage like traditional BI ignores additional risks around lineage, retrieval, sensitivity, and model behavior.                           |
| Ignoring AI-specific data risks                 | Creating policies without operational workflows       | AI governance principles are ineffective unless they are translated into data source approval, access review, lineage tracking, and monitoring workflows. |

---

## How to Use This Matrix

Use this matrix as a diagnostic tool.

If a governance program shows one anti-pattern, check whether related anti-patterns are also present. For example:

* If governance is treated as an IT-only initiative, check whether the governance council has real business decision rights.
* If success is measured by catalog coverage, check whether the team is trying to govern too much at once.
* If AI use cases are moving quickly, check whether existing data governance controls are sufficient for AI-specific risks.

The goal is not to eliminate every anti-pattern immediately. The goal is to identify the highest-risk failure mode and correct it before scaling the governance program.
