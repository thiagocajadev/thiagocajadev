# SDD Deep-Flow: Inside the Work Cycle

This guide explains how an AI assistant configured to work with SDD (Spec-Driven Development) organizes its thinking at each phase of the project. The goal is to ensure that the work is transparent, secure, and easy to follow.

Note\*: The development team can also follow this flow without agents; it is a strategic choice.

I invite you to explore the web guide for more content and visual representations at [specdrivenguide.org](https://specdrivenguide.org)

---

## Visualizing the Deep-Flow

The following diagram illustrates the transitions between phases, the key decision points, and how we ensure architectural integrity.

<details>
<summary>Click to visualize the internal Deep-Flow</summary>

```mermaid
graph TD
    Trigger((Request)) --> SPEC

    subgraph SPEC [1. SPEC: The Contract]
        S1[Intent Classification] --> S2[Goal Definition]
        S2 --> S3[Domain & Contracts]
        S3 --> S4[Checklist Verification]
        S4 --> S5{Approval Barrier}
    end

    S5 -- Approved --> PLAN
    S5 -- Denied --> SPEC

    subgraph PLAN [2. PLAN: The Strategy]
        P1[Decomposition of Tasks] --> P2[Logical Sequencing]
        P2 --> P3[Effort Tagging]
        P3 --> P4[Sub-task Split]
        P4 --> P5[Backlog Sync]
        P5 --> P6{Approval Barrier}
    end

    P6 -- Approved --> CODE
    P6 -- Denied --> PLAN

    subgraph CODE [3. CODE: The Execution]
        C1[Context Load] --> C2[Narrative Barrier]
        C2 --> C3[Plan Adherence]
        C3 --> C4[Blocker Surface]
    end

    C4 -- No Progress Loop 3x --> Stop
    C4 --> TEST

    subgraph TEST [4. TEST: The Verification]
        T1[Checklist Verification] --> T2[Regression Proof]
        T2 --> T3{Fix Loop}
        T3 -- Success --> T4[Lint Fix]
        T4 --> T5[Status Report]
    end

    T3 -- Failure (Max 3x) --> CODE
    T3 -- Blocked --> Stop((STOP & Report))

    T5 --> END

    subgraph END [5. END: The Delivery]
        E1[Task Summary] --> E2[CHANGELOG]
        E2 --> E3[Backlog Sync]
        E3 --> E4[Context & Insights]
        E4 --> E5[Final Verification (Lint)]
        E5 --> E6[Commit Suggestion]
        E6 --> E7[Next Steps]
    end

    E7 --> Done((Done))

    style S5 fill:#f96,stroke:#333
    style P6 fill:#f96,stroke:#333
    style T3 fill:#f96,stroke:#333
    style C4 fill:#ffa,stroke:#333
    style Stop fill:#f66,stroke:#333
```

</details>

---

## What happens in each phase?

### 1- Phase: SPEC (The Contract)

> **Role: Planning**

The agent defines **what** to build before thinking about **how**. It is the moment to align expectations.

- **Intent Identification**: Classification as `feat:`, `fix:`, or `docs:`.
- **Goal**: A technical "North Star" sentence.
- **Verification Checklist**: Up to 5 binary criteria used to validate the final delivery.
- **Approval Barrier (Gate)**: Execution **must stop** here for **Developer verification**.

### 2- Phase: PLAN (Planning)

> **Role: Planning**

The agent transforms the spec into smaller tasks with effort estimates.

- **Tasks**: Decomposition into tasks (Action Verb + Object).
- **Effort Tagging**: Tasks classified by size — `[S]` (small), `[M]` (medium), or `[L]` (large).
- **Sub-task Split**: Any `[L]` task is decomposed into smaller steps.
- **Approval Barrier**: Execution stops again here for strategy approval.

### 3- Phase: CODE (The Execution)

It is time to get hands-on with the code, following organizational best practices.

- **Narrative Code**: Self-check for architectural standards like the **Linear Writing Rule (Stepdown Rule)**.
- **Plan Adherence**: No features or refactors outside of scope (YAGNI: "You Ain't Gonna Need It").
- **Blocker Surface**: The agent flags issues immediately instead of working around them.
- **Circuit Breaker**: If the same error repeats 3 times, or no progress is made, the agent **stops and reports** instead of continuing in a loop.

### 4- Phase: TEST (The Verification)

The agent checks if everything built matches the original Spec checklist.

- **Regression Proof**: For bugs, the agent must prove the fix works without breaking existing logic.
- **Fix Loop**: A resilience mechanism that allows up to **3 refactor attempts** if tests fail. After that, it requests human intervention.
- **Lint Fix**: Automated resolution of style problems in the code before reporting success.

### 5- Phase: END

> **Role: Planning**

Closing the cycle and ensuring project observability.

- **Artifact Sync**: Updates to `tasks.md` (status DONE) and `context.md` (next objective).
- **Engineering Insights**: The agent records research findings, rework patterns, and lessons learned in `context.md ## Engineering Insights`.
- **Changelog**: Consistent history following the [Keep a Changelog](https://keepachangelog.com/) standard.
- **Semantic Commit**: Proposed commit message that reflects the actual intent and scope of the change.

---

> [!TIP]
> This internal flow is the map that guides the agent. Knowing these steps helps you understand **why** it asks certain questions and **where** it checks the quality of the work.
