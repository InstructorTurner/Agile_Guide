# ☁️ Azure DevOps (ADO) Basics

## 📋 Board Management for Scrum
| Action | Description |
| :--- | :--- |
| **Epic** | Large initiatives (Quarterly goals) |
| **Feature** | Deliverable functionality (Sprint goals) |
| **User Story** | Small, testable units of value (Sprint tasks) |
| **Task** | Technical implementation steps for a Story |

### Sprint Workflow
1.  **Backlog:** Stories are refined and prioritized.
2.  **Sprint Planning:** Move Stories from Backlog to the current Sprint.
3.  **Board:** Move cards from `To Do` $\rightarrow$ `Doing` $\rightarrow$ `Done`.
4.  **Update:** Ensure every Task is linked to a User Story.

## 🌿 Branching Strategy: Small Feature Branches
To keep the codebase stable and reviews manageable, we follow a "Small Feature Branch" approach.

### The Workflow
1.  **Create:** Branch off `main` for a specific User Story.
    *   *Naming:* `feature/story-id-short-description` (e.g., `feature/102-user-auth`)
2.  **Commit:** Make small, frequent commits with descriptive messages.
3.  **PR:** Open a Pull Request early.
4.  **Merge:** Once approved and CI passes, merge into `main` and delete the branch.

### ⚠️ Key Rules
*   Never commit directly to `main`.
*   One branch = One Story. If the story is too big, break it down.
