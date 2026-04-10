# SDD Deep-Flow: Inside the Cycle

This guide provides a detailed visual and technical breakdown of the internal sub-steps that an **SDG-compliant AI Agent** executes during each phase of the task cycle.

*Note: The development team can also follow this flow without agents; it is a strategic choice.*

I invite you to explore the web guide for more content and visual representations at [specdrivenguide.org](https://specdrivenguide.org)

## Visualizing the Deep-Flow

The following diagram illustrates the transitions, decision barriers, and loops that ensure architectural integrity.

<details>
<summary>Click to visualize the internal Deep-Flow</summary>

```mermaid
graph TD
    Trigger((Request)) --> SPEC

    subgraph SPEC [1. SPEC: The Contract]
        S1[Intent Classification] --> S2[Goal Definition]
        S2 --> S3[Domain & Contracts]
        S3 --> S4[Verification Checklist]
        S4 --> S5{Approval Barrier}
    end

    S5 -- Approved --> PLAN
    S5 -- Denied --> SPEC

    subgraph PLAN [2. PLAN: The Strategy]
        P1[Task Decomposition] --> P2[Logical Sequencing]
        P2 --> P3[Effort Tagging]
        P3 --> P4[Sub-task Split]
        P4 --> P5[Backlog Sync]
        P5 --> P6{Approval Barrier}
    end

    P6 -- Approved --> CODE
    P6 -- Denied --> PLAN

    subgraph CODE [3. CODE: The Execution]
        C1[Context Load] --> C2[Narrative Gate]
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
        E4 --> E5[Final Lint]
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

## Detailed Phase Breakdown

### 1. Phase: SPEC

> **Role: Planning**

The agent defines **what** to build before thinking about **how**.

- **Intent Identification**: Classification as `feat:`, `fix:`, or `docs:`.
- **Goal**: A technical "North Star" sentence.
- **Verification Checklist**: Up to 5 binary criteria used to validate the final delivery.
- **Approval Gate**: Execution **must stop** here for **Developer verification**.

### 2. Phase: PLAN

> **Role: Planning**

The agent transforms the spec into smaller tasks with effort estimates.

- **Tasks**: Pattern: `Action Verb + Object`.
- **Effort Tagging**: Tasks classified by size — `[S]` (small), `[M]` (medium), `[L]` (large).
- **Sub-task Split**: Any `[L]` task is decomposed into smaller steps (`1.1`, `1.2`).
- **Approval Gate**: Execution **must stop** here to ensure the strategy is sound.

### 3. Phase: CODE

> **Role: Coder**

Execution following architectural standards.

- **Narrative Barrier**: Self-check for **Stepdown Rule**, **SLA**, and **Lexical Scoping**.
- **Plan Adherence**: No features or refactors outside of scope (YAGNI).
- **Blocker Surface**: The agent flags issues immediately instead of working around them.
- **Circuit Breaker**: If the same error repeats 3 times, or no physical progress (file writes, commands) is made in 3 consecutive turns, the agent **stops and reports** instead of continuing in a loop.

### 4. Phase: TEST

> **Role: Coder**

Verification comparing against the original Spec checklist.

- **Regression Proof**: For bugs, the agent must prove the fix works without breaking existing logic.
- **Fix Loop**: A resilience mechanism that allows up to **3 refactor attempts** if tests fail. On the third failure, the Circuit Breaker is triggered — the agent stops and reports.
- **Lint Fix**: Automated resolution of style problems in the code before reporting success.

### 5. Phase: END

> **Role: Planning**

Closing the loop and ensuring project observability.

- **Artifact Sync**: Updates to `tasks.md` (status DONE) and `context.md` (next objective).
- **Engineering Insights**: The agent records research findings, rework patterns, and lessons learned in `context.md ## Engineering Insights`. Obsolete entries are removed, keeping the file lean between sessions.
- **Changelog**: Consistent history following the [Keep a Changelog](https://keepachangelog.com/) standard.
- **Semantic Commit**: Proposed commit message that reflects the actual intent and scope of the change.

---

> [!TIP]
> This deep-flow is an internal reference model for the agent. Use it to understand the **whys**, **what for**, and **where to** the agent checks at each barrier.
