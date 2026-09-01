# Git Best Practices for Agile Teams

This guide provides foundational best practices for managing source code collaboratively in an Agile environment. Git is powerful, but without consistent, clean habits, it can become a source of significant technical debt and friction.

**The Core Philosophy:** The goal of Git hygiene is to ensure that the `main` or `develop` branch is *always* in a healthy, potentially deployable state. We aim for small, frequent, uncontroversial contributions.

---

**Key Principles to Adopt:**

1.  **Always Commit Small and Atomic:** A commit should represent a single, cohesive change. If you fixed a bug and refactored a function—make two separate commits. This makes history readable and acts as a safety net.
2.  **Short-Lived Branches:** Branches should exist for the absolute minimum amount of time required to complete a unit of work. Long-lived branches inevitably drift from the main codebase, creating painful, massive merge conflicts.
3.  **Frequent Integration:** The most vital habit. Do not wait until a feature is "done" to merge. Integrate small bits of working code into the shared development branch *often*. This allows the team to catch integration conflicts hours after they happen, instead of weeks later.

### 🔄 The Git Flow Paradigm: Embracing Trunk-Based Development (TBD)

For Agile teams, we strongly recommend adhering to the principles of **Trunk-Based Development (TBD)**.

**What is TBD?**
Instead of creating massive feature branches (which can live for days or weeks), TBD advocates for developers to commit small, incomplete, or experimental code directly to a main development trunk (e.g., `develop`).

**Why is it better for Agile?**
*   **Reduces Merge Hell:** Because branches are so short-lived (sometimes minutes), conflicting changes are small and easy to resolve immediately.
*   **Faster Feedback:** The integration effort happens continuously, ensuring the codebase remains stable and rapidly responsive to feedback.

**The Workflow Principle:** The main development branch is the current truth. Your goal is to make your small slice of truth merge into that truth as quickly as possible.

---
