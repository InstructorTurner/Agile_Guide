## Trunk-Based Development (TBD)

In an agile environment, branching strategy is not about protecting code; it's about *managing integration*. For highly collaborative, high-velocity teams, we mandate the use of Trunk-Based Development (TBD).

### 🌳 What is Trunk-Based Development?

TBD is a workflow where all developers commit small, incremental changes directly or almost directly to a single, primary, stable branch—the "trunk" (e.g., `develop`). The core idea is *integration over isolation*.

**Concept:** Instead of creating a large `feature/my-epic-feature` branch that might live for two weeks, a developer checks in one small, isolated piece of the feature (a few lines of code implementing a specific function) every few hours.

### 🛠️ Implementing TBD Best Practices

1.  **Flags and Feature Toggles (The Key Tool):** Since you cannot commit half-finished features to the main trunk, TBD necessitates the use of **Feature Toggles** (or Feature Flags).
    *   **Definition:** A feature flag is a simple configuration switch in the codebase that allows a feature to be merged into the main branch and committed, but remains functionally "off" (disabled) in the production/staging environment until the business is ready to turn it on.
    *   **Benefit:** This allows feature code to be integrated and tested *live* against the main codebase without requiring a full release, eliminating long-lived branches.

2.  **Branch Lifetime:**
    *   **Rule:** A branch should only exist to isolate a single, small unit of work. If the work takes longer than a few hours, the change must be broken down into smaller commits.
    *   **Avoid:** Large, long-running integration branches. These are the primary source of merge conflicts ("Merge Hell"), where conflicts become so complex that developers spend days or weeks untangling them.

3.  **Commit Discipline:**
    *   **Atomic Commits:** Each commit must do one thing, and only that thing. A commit should be self-contained and logically sound.
    *   **Small Batches:** Commit small changes frequently. This minimizes the scope of any single conflict and makes the Git history a narrative of small, successful steps.

***
**Summary:** TBD makes the main branch the truth at all times. It trades the perceived safety of isolation (long branches) for the proven reliability of constant, small integration.

**Next Up:** Now that we know *how* to branch, the next critical step is to define the safe process for merging that work into the main trunk: the Pull Request. This will go into `02_the_pull_request_process.md`.