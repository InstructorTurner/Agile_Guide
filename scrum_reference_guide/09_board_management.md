---
layout: page
title: Board Management
---

# 📋 09: Scrum Board Management - Visualizing Flow

**Goal:** To maintain a "single source of truth" for the Sprint's progress and identify bottlenecks early.

## ⚙️ The Mechanics (The Setup)

A Scrum board visualizes the workflow from a backlog item's inception to its completion.

*   **Columns:** A standard flow typically looks like: 
    `To Do` -> `In Progress` -> `Testing/Review` -> `Done`.
*   **WIP Limits (Work In Progress):** This is a cap on how many items can be in a specific column at once. It enforces a **"Stop Starting, Start Finishing"** mindset, preventing the team from multitasking and stalling several stories at once.
*   **Card Hygiene:** Cards must be updated in real-time. If a developer starts a task, it moves immediately. If a task is blocked, it is flagged immediately.

## 🔄 The Ritual (The Usage)

The board is not just a status report; it is a tool for the Daily Scrum.

*   **Walking the Board:** Instead of "What did I do yesterday?", the team "walks the board" from **right-to-left** (`Done` <- `To Do`). This focuses the conversation on the items closest to completion and asks, "What do we need to do to get this card into the Done column?"
*   **Identifying Blockers:** Use visual cues (red flags, stickers, or tags) for impeded items. These are the primary focus of the Daily Scrum.
*   **The "Done" Transition:** A card only moves to `Done` when it meets the **Definition of Done** (see `07_definitions.md`). No "99% done" cards allowed.

## 🛠️ Inspect and Adapt: Evolving the Board

The board is not a static artifact; it is a tool owned by the developers. If the team discovers during a **Retrospective** that the board doesn't accurately reflect their workflow or is hiding bottlenecks, they should change it.

**Examples of board evolutions:**

*   **Adding a "Ready for Test" Column:** If cards pile up in `In Progress` because they are waiting for a tester, adding a specific handover column makes the bottleneck visible.
*   **Creating a "Blocked" Area:** Instead of just flagging a card, moving it to a dedicated "Blocked" zone can highlight systemic issues that need the Scrum Master's attention.
*   **Adjusting WIP Limits:** If the team realizes they are still multitasking too much, they may lower the WIP limit on the `In Progress` column to force more focus on completion.

## ⚠️ Anti-Patterns & Red Flags

Watch for these signs that the process is breaking down:

*   **The "Waterfall" Board:** All cards stay in `In Progress` for 90% of the sprint, then all move to `Done` on the final day. This indicates a lack of vertical slicing.
*   **The "Ghost" Column:** Cards that pile up in `Testing` or `Review` for days. This is a bottleneck that requires the whole team to swarm and fix.
*   **The "Invisible Work" Trap:** Team members mentioning work during the Daily Scrum that isn't represented by a card on the board. If it's not on the board, it doesn't exist.
*   **The "Overloaded" Column:** Ignoring WIP limits, leading to a massive pile-up in one stage while other team members are idle or starting new work.

---
*🔗 Context: Find your place in the overall curriculum here.*
**[📘 Scrum Fundamentals Reference Guide](./index.md)**
