# Governance

> Scope: cross-cutting. Applies to any language or stack in the project.

Governance is the decision about how the project is understood and navigated, as well as how it is
built. A well-governed project is one where anyone, from non-technical people to experts, can
navigate, understand, and contribute with context.

## Fundamental concepts

| Concept | What it is |
|---|---|
| **SDLC** (Software Development Life Cycle) | The set of development phases: design, implementation, testing, delivery, operation, and maintenance |
| **ADR** (Architecture Decision Record) | A document that records the reasoning behind a technical decision, the alternatives considered, and the consequences |
| **Onboarding** | The process of integrating a new member into the project, transferring structural knowledge |
| **Landing** (first contact) | The project's entry point; what a dev sees first when opening the repository |

## Convictions

**Code serves the team.** The best solution is the one the next dev can read, maintain, and evolve
with confidence. Elegance without readability has limited value.

**Governance over the full cycle.** Every technical decision has consequences beyond the present
moment: on maintenance, on onboarding, on the team's scalability. Thinking about governance is
anticipating these consequences before writing them into the code.

**Summarized complexity.** Every system has inherent complexity. The job is to organize it into
accessible layers: from the non-technical person who needs to understand what the system does, to
the expert who needs to understand why each decision was made.

**Consistency as a multiplier.** Predictable patterns reduce cognitive load. A dev who learns how
one module works learns them all. Consistency scales the team without scaling training.

**Process, not people.** When something fails, the focus goes to the process that allowed the
failure, not to who executed it. Blaming people does not solve the problem. Understanding what in
the process failed, and fixing it, is what prevents the failure from recurring.

## The Staff Engineer mindset

The **SDLC** (Software Development Life Cycle) starts before the first commit and ends after the
last deploy. Design, implementation, testing, delivery, operation, and maintenance: each phase
weighs on the decisions the engineer makes today.

Staff engineers think in systems. The question guiding the work shifts from "how do I implement
this?" to "how does this affect the team that will maintain it, the dev that will onboard, the
product that will grow?".

This translates into constant questions before any decision:

- Who is going to maintain this code in six months?
- Can a new dev understand what this module does without asking for help?
- Does today's decision create or reduce future complexity?
- Does the pattern established here apply to the rest of the system?

The answer to these questions is what separates code that works from code that serves the team.

## Landing and Onboarding

Landing is the first contact with the project. What a dev sees first determines whether the project
feels accessible or opaque.

A good landing is hierarchical: from general to specific, from concept to implementation.

```
README                → what it is, how to run it, where to find what
docs/shared/          → language- and platform-agnostic principles
docs/<language>/      → stack-specific conventions
quick-reference.md    → quick reference for already-onboarded devs
```

The README is the front door. Someone who has never seen the project must be able to, in under 5
minutes: understand what the project does, run it locally, and know where to look for what they
need. If they have to ask for help on any of these three, the README is incomplete.

Effective onboarding transfers structural knowledge, not point-by-point knowledge. A dev who
understands how one module is organized understands all the others, because the pattern is the
same. The project's consistency is what makes onboarding scalable.

## Layered Complexity

A system's complexity exists. Governance is about presenting it in the right dose, to the right
audience, at the right time.

Layered documentation serves this purpose:

| Audience        | What they need                                   | Where to find it                   |
| --------------- | ------------------------------------------------ | ---------------------------------- |
| Non-technical   | Understand what the system does and how it's organized | README, conceptual docs      |
| Starting dev    | Run it, contribute, understand conventions       | README, quick-reference, examples  |
| Experienced dev | Details of patterns and architecture decisions   | docs/shared, ADRs                  |
| Expert          | Reasoning behind each technical choice           | ADRs, decision comments            |

When any of these audiences opens the project and says "got it", governance is working.

## Naming as Governance

Names are the cheapest and most efficient governance mechanism. An expressive name communicates
intent without additional documentation.

The cost of a bad name scales with time: every dev who reads `data`, `helper`, or `utils` has to
trace where it came from and what it does. An expressive name pays that debt once, at writing time.

Consistent naming creates a shared vocabulary. When the whole codebase uses `fetch` for reads,
`save` for writes, and `calculate` for derivation, the reader knows what to expect from any
function they haven't seen yet. The project speaks one language, and any new member learns the
vocabulary once.

## Consistency as a Multiplier

Consistency reduces cognitive load. When patterns are predictable, the reader spends energy
understanding the domain, not deciphering the style.

The practical consequence: a dev who understands how one module is structured understands them all.
Onboarding into one area of the system transfers to all the others. Consistency scales the team
without scaling training.

Inconsistency has the opposite effect. Each module demands re-learning. The team grows, but
knowledge transfer doesn't work, because each part of the system "has its own way".

## Decision Records

**ADRs** (Architecture Decision Records) document the *why* of decisions, not just the *what*. Code
shows what was done. The ADR shows why it was done this way and which alternatives were considered.

Undocumented decisions become lore: knowledge that exists only in the heads of those who were
present. When those people leave, the knowledge goes with them. Whoever arrives later questions the
decision, redoes the analysis, and sometimes reverts something that had a legitimate reason.

Three elements make an ADR useful:

| Element          | Content                                                         |
| ---------------- | --------------------------------------------------------------- |
| **Context**      | The problem that existed and the constraints at the time        |
| **Decision**     | What was chosen and why                                         |
| **Consequences** | What gets better, what gets worse, what needs attention         |

## Code Review as Governance

Code review is where governance meets execution. A review that only checks for bugs misses the
opportunity to check whether the code fits the system.

Questions that guide a review with a governance mindset:

- Does the name of this function make sense to someone who has never seen the context?
- Is this pattern consistent with the rest of the module?
- Was the documentation updated for this change?
- Will the person maintaining this in a year understand it without additional context?

The goal of the review is code that will last, not quick approval. A rigorous review on code that
will live for years is worth more than a shallow review that passes quickly.

## Auditable Process

A process is good when it becomes auditable. Auditable means that at any point of the cycle it is
possible to measure quality without depending on memory or on who was present.

Each stage has an input, an output, and a verifiable criterion. When this is in order, anyone (dev,
tech lead, business people) can inspect a single point or the whole cycle and assess the real state
of the project.

```
Spec → Implementation → Review → CI → Deploy → Observation
```

| Stage          | Output                                      | What is auditable                    |
| -------------- | ------------------------------------------- | ------------------------------------ |
| Spec           | ADR, ticket, acceptance criteria            | Recorded and traceable decisions     |
| Implementation | Code + tests                                | Git history, coverage                |
| Review         | PR with approvals and feedback              | Traceability of each change          |
| CI             | Build + lint + automated tests              | Pass/fail per commit                 |
| Deploy         | Versioned artifact, who + when + where      | Delivery traceability                |
| Observation    | Logs, metrics, alerts                       | Real state in production             |

> The order and stages may vary depending on project type, scope, and team split. What matters is
> having clarity about each stage and ensuring all of them are executed.

The sign that the process is auditable: when a failure happens in production, each stage answers
through its own record. Which decision originated the problem, which review it passed through,
which test did not cover it, which deploy introduced it. The team finds the answers without
relying on memory.

## Checklists as a Quality Tool

When the process is aligned, quick verification checklists work as a natural control tool. Each
stage has its own checklist: lightweight, specific, and applied at the right moment.

The goal is to catch non-conformities before they propagate. An item not checked in the Spec
becomes rework in the Review. An item not checked in the Review becomes a bug in production.

| Stage          | Examples of verification                                                     |
| -------------- | ---------------------------------------------------------------------------- |
| Spec           | Acceptance criteria defined? Decision recorded in an ADR or ticket?          |
| Implementation | Do tests cover the critical paths? Does the naming follow the conventions?  |
| Review         | Pattern consistent with the rest of the module? Documentation updated?       |
| CI             | Build passes? Lint with no warnings? Coverage within the threshold?          |
| Deploy         | Identifiable version? Rollback mapped? Feature flag active if needed?        |
| Observation    | Structured logs? Alert configured? Baseline metrics recorded?                |

Checklists do not replace judgment. They exist so you don't forget the obvious under pressure.

## Standards as a Basis for Decision

A decision backed by a standard stops being opinion and becomes traceable. When a technical choice
can point to an **RFC** (Request for Comments, from the IETF), **ISO** (International Organization
for Standardization), or another recognized standard, the team gains a shared basis that does not
depend on individual authority.

The standard does not replace judgment. It replaces unproductive discussion. When two people
disagree about "how to do authentication", the conversation shifts from personal preference to a
shared reading of RFC 6749 (OAuth2). The same applies to software quality, information security,
and incident response.

| Standard                  | Scope                                          | When to reference                                         |
| ------------------------- | ---------------------------------------------- | --------------------------------------------------------- |
| **RFC 2119**              | Requirement vocabulary (MUST, SHOULD, MAY)     | Specifications, ADRs, acceptance criteria                 |
| **RFC 6749 / 7519**       | OAuth2 and JWT                                 | Decisions about authentication and tokens                 |
| **RFC 7231 / 9110**       | HTTP semantics                                 | API definition, verbs, and status codes                   |
| **ISO/IEC 25010**         | Software quality                               | Trade-offs of performance, maintainability, security      |
| **ISO/IEC 27001**         | Information security                           | Policies, controls, audit                                 |
| **ISO/IEC 27035**         | Incident management                            | Incident response playbooks                               |
| **ISO 8601**              | Date and time representation                   | API contracts, logs, temporal persistence                 |
| **OWASP ASVS / Top 10**   | Application security verification              | Hardening checklist, security review                      |
| **SemVer 2.0.0**          | Software versioning                            | Releases, API contracts, dependency management            |
| **Conventional Commits**  | Commit message standard                        | Git history, automated changelogs                         |

> Standards are a reference, not dogma. In a context where the standard limits the outcome, record
> in the ADR why the deviation. A documented deviation is as valuable as conformance.

The sign that the culture is mature: ADRs start citing standards. Reviews start referencing RFCs.
The discussion moves away from "I think" and into "standard X says Y, here we deviate because of Z".

## The Sign That Governance Is Working

The clearest sign: people from different contexts can interact with the project with confidence.

The non-technical person understands what the system does and how it is organized. The new dev
contributes in days, without having to ask for context. The experienced dev locates what they need
without asking. The expert finds the reasoning behind the decisions.

When any of them opens the project and says "this was easy to understand", governance has fulfilled
its purpose.
