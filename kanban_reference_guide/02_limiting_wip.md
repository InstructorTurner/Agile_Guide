---
layout: page
title: Limiting Wip
---

## Limiting Work In Progress (WIP)

If the Kanban board shows *where* work is, then setting Work In Progress (WIP) Limits tells the team *how much* work they should be focusing on right now. This is arguably the single most important concept in Kanban.

### 🛑 What is WIP?

**Work In Progress (WIP)** is simply the number of tasks that are currently being actively worked on at any given moment.

In a typical non-Kanban approach, developers often pull tasks into "In Progress" without consulting the limits, leading to overcommitment—juggling too many things at once. This is called **Work Overload**.

### 📐 The Power of the Limit

A WIP Limit is a cap—a maximum number of items that can exist in a specific column (e.g., "In Progress" can never hold more than 3 items).

**Why is this critical?**
When a WIP Limit is hit, the team is **forced to stop pulling new work**. This mandatory pause shifts the team's collective attention entirely to the items that are already in progress.

**Benefits of Applying WIP Limits:**
1.  **Reduces Context Switching:** Switching between tasks (context switching) is mentally expensive and dramatically slows down completion rates. WIP limits force focus.
2.  **Highlights Bottlenecks:** When the "Review/QA" column hits its limit of 2, but the "In Progress" column has 5 items waiting to be reviewed, the constraint is immediately visible. This signals that the QA team is the system bottleneck, and the team must swarm to help them.
3.  **Creates Flow:** By limiting work, the team optimizes for *flow*—getting items across the finish line quickly—rather than optimizing for *occupancy* (keeping everyone busy).

### 🏃 Flow Management: The Principle of "Pull"

Kanban operates on a **Pull System**:
*   Work items are **Pulled** into the next stage *only when* capacity exists at the next stage, and *only* after the WIP limit for that stage allows it.
*   It is not a "Push" system (i.e., "We finished doing X, so we will *push* it to the next person regardless of their capacity").

**Team Responsibility:** Every team member is responsible for maintaining optimal flow. When a developer finishes their task, their first action is not to grab a new task but to ensure the completed task is handed off to clear the *next* person's queue, thus helping "pulling" the flow forward.

***
**Key Takeaway:** The goal is not to be busy; the goal is to achieve maximum *throughput* (the rate of completed, valuable work). WIP limits are the guardrails that make that possible.
