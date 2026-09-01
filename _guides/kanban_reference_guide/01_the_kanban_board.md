---
collection: guides
layout: page
title: The Kanban Board
---

## The Conceptual Kanban Board

The Kanban board is the single most important artifact in the Kanban system. It is a physical or digital visual representation of the entire workflow that an item (a User Story, a task, a bug fix) goes through from conception to completion.

**Goal of the Board:** To make the invisible work, potential bottlenecks, and constraints visible to everyone on the team. It forces transparency and shared understanding of the process.

### Structure and Workflow States

The board translates abstract process steps into tangible columns. Every column represents a defined *status* that the work item must pass through.

**Common Workflow Stages (Columns):**
1.  **Backlog / To Do:** Where all potential work items (stories, ideas) reside. They are prioritized but haven't been committed to the current cycle.
2.  **Ready / To Pull:** These items are small, fully defined, and prioritized, meaning the team is ready to pull them into active work.
3.  **In Progress (WIP):** The work item is being actively developed (writing code, designing, etc.).
4.  **Review / QA:** The work item is complete from a development standpoint but must be validated by peers or quality assurance.
16: 5.  **Done:** The item meets the Definition of Done (DoD), is tested, and provides demonstrable business value.
    *   *See the Scrum Guide for a detailed look at how we define 'Done':* **[07_definitions.md](../scrum_reference_guide/07_definitions.md)**

**📌 Key Learning:** The board is not static. As the team learns and the project evolves, the columns and steps on the board should be adjusted. This is part of continuous improvement.

### 🤝 How Collaboration Works with the Board

The board is the physical embodiment of *collaboration*.
*   **Single Source of Truth:** Everyone consults the board first. It prevents developers from asking, "What are we working on?"
*   **Visualizing Flow:** By looking at the board, the entire team can immediately see where the largest bottlenecks are. If the "Review/QA" column is constantly overflowing, the team knows they need to dedicate more resources or time to testing—the bottleneck is visually apparent.
*   **The Hand-off:** Moving a card (task) from one column to the next represents a formal hand-off of responsibility. The team takes collective ownership at every stage.

**🛠️ Tooling Tips:**
Depending on the tool we use (e.g., **Trello** or **Azure DevOps Boards**), the way we visualize WIP limits may vary. Some tools have built-in WIP counters at the top of the column, while others require us to manage them manually via labels or team agreements. Regardless of the tool, the *rule* remains the same: do not pull if the limit is reached.

***
**Key Takeaway:** The Kanban board shifts the team's focus from *time* (like Scrum focuses on fixed timeboxes) to *flow* and *process efficiency*.
