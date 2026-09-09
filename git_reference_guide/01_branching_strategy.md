---
layout: page
title: Branching Strategy
---

## Short-Lived Feature Branches

In an agile environment, branching strategy is not about protecting code; it's about *managing integration*. To maintain high velocity and reduce the risk of massive merge conflicts, we use a **Short-Lived Feature Branch** model.

### 🌳 Integration Over Isolation

The core idea is to avoid "long-running" branches. Instead of creating a massive `feature/my-epic-feature` branch that might live for two weeks, we break the work into the smallest possible functional units (Vertical Slices) and merge them into the `develop` branch as soon as they are ready.

**The Concept:**

1.  Create a branch using the naming convention (e.g., `feat/add-login`).
2.  Implement the change.
3.  Open a PR, get peer approval, and merge.
4.  Delete the branch and repeat for the next slice.

### 🛠️ Best Practices for Branching

#### Branch Naming Conventions
To keep the repository organized, use the following pattern: `type/description`

*   `feat/`: New functionality.
*   `fix/`: Bug fixes.
*   `chore/`: Maintenance, dependency updates, or tooling.
*   `refactor/`: Code changes that neither fix a bug nor add a feature.
*   `docs/`: Documentation-only changes.

#### Branch Lifetime (The 48-Hour Rule):
*   **Goal:** Aim to merge your branch into `develop` within 24-48 hours. 
*   **Why?** The risk of a merge conflict scales exponentially with the age of the branch. A branch that lives for a week is a liability; a branch that lives for a day is a tool.
*   **Action:** If your task is too big to merge in two days, it is not a "slice"—it is a "chunk." Break it down further.
*   This is about code, not features.  You don't need to have a feature done within 48 hours, but you should try to have some part of your code available to merge into the main branch on a regular basis to keep everyone updated.

#### Keeping Branches Current:
To avoid massive conflicts at the end of your slice, regularly bring changes from `develop` into your feature branch.

*   **Strategy:** Use `git merge develop` while on your feature branch.
*   **Why?** We prefer merge over rebase for simplicity and to preserve the accurate history of how the code evolved.

#### Managing Incomplete Work:
Since we merge frequently, you might merge code that isn't fully "visible" to the user yet.

*   **Hidden Endpoints:** Create the API endpoint but don't link it to the UI yet.
*   **Internal Interfaces:** Build the logic and verify it with tests, then merge it before the UI is even started.
*   **Feature Flags:** For larger changes that must be merged but not activated, use Feature Toggles (configuration switches) to keep the code dormant in production.

#### Commit Discipline:
*   **Atomic Commits:** Each commit must do one thing, and only that thing.
*   **Small Batches:** Commit small changes frequently. This minimizes the scope of any single conflict and makes the Git history a narrative of small, successful steps.

#### Post-Merge Cleanup:
Once a branch is merged into `develop`, **delete it immediately**. 

*   Local: `git branch -d branch-name`
*   Remote: `git push origin --delete branch-name`
This prevents "branch bloat" and ensures the team only focuses on active work.

***
**Summary:** We prioritize constant, small integration over the perceived safety of isolation. By keeping branches short-lived, we ensure that the `develop` branch remains the single source of truth and that merge conflicts remain trivial.
