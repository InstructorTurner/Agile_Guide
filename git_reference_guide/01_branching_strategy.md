## Short-Lived Feature Branches

In an agile environment, branching strategy is not about protecting code; it's about *managing integration*. To maintain high velocity and reduce the risk of massive merge conflicts, we use a **Short-Lived Feature Branch** model.

### 🌳 Integration Over Isolation

The core idea is to avoid "long-running" branches. Instead of creating a massive `feature/my-epic-feature` branch that might live for two weeks, we break the work into the smallest possible functional units (Vertical Slices) and merge them into the `develop` branch as soon as they are ready.

**The Concept:**
1.  Create a branch for a single, small unit of work.
2.  Implement the change.
3.  Open a PR, get peer approval, and merge.
4.  Delete the branch and repeat for the next slice.

### 🛠️ Best Practices for Branching

1.  **Branch Lifetime (The 48-Hour Rule):**
    *   **Goal:** Aim to merge your branch into `develop` within 24-48 hours. 
    *   **Why?** The risk of a merge conflict scales exponentially with the age of the branch. A branch that lives for a week is a liability; a branch that lives for a day is a tool.
    *   **Action:** If your task is too big to merge in two days, it is not a "slice"—it is a "chunk." Break it down further.

2.  **Managing Incomplete Work:**
    Since we merge frequently, you might merge code that isn't fully "visible" to the user yet.
    *   **Hidden Endpoints:** Create the API endpoint but don't link it to the UI yet.
    *   **Internal Interfaces:** Build the logic and verify it with tests, then merge it before the UI is even started.
    *   **Feature Flags:** For larger changes that must be merged but not activated, use Feature Toggles (configuration switches) to keep the code dormant in production.

3.  **Commit Discipline:**
    *   **Atomic Commits:** Each commit must do one thing, and only that thing.
    *   **Small Batches:** Commit small changes frequently. This minimizes the scope of any single conflict and makes the Git history a narrative of small, successful steps.

***
**Summary:** We prioritize constant, small integration over the perceived safety of isolation. By keeping branches short-lived, we ensure that the `develop` branch remains the single source of truth and that merge conflicts remain trivial.

**Next Up:** Now that we know *how* to branch, the next critical step is to define the safe process for merging that work into the main trunk: the Pull Request. This will go into `02_the_pull_request_process.md`.