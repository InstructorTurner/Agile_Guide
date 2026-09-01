---
layout: page
title: Classes Of Service
---

## Classes of Service (CoS)

When managing flow, not all incoming work is created equal. A small bug fix might be vital, while a new feature might be helpful, and a compliance requirement might be mandatory. Kanban addresses this by defining **Classes of Service (CoS)**.

A CoS is a designated category (a lane, a color, or a specific label) that dictates the priority, required focus, and expected flow behavior for an item *before* it ever hits the board.

### 🏷️ Defining the Service Categories

While specific teams may customize these, most Kanban implementations use a framework similar to this:

1.  **Expedite (The Emergency):**
    *   **Definition:** Work with the highest possible priority, requiring immediate attention.
    *   **Flow Impact:** This is typically a break-glass scenario (e.g., a production outage). It *must* jump the queue, often overriding existing WIP commitments.
    *   **Caution:** This category should be used extremely rarely. If it's used often, it indicates systemic instability that needs root-cause analysis.

**⚠️ Avoiding the "Expedite Trap":**
When an Expedite item enters the flow, the team's instinct is to drop everything. To maintain collaboration and stability:
*   **Dedicated Resource:** If possible, assign one person to the emergency while others maintain the current WIP limits for Standard work.
*   **Transparent Communication:** Immediately notify the team and PO that "Standard" work will slow down because of the Expedite item.
*   **Post-Emergency Review:** Always discuss Expedite items in the next Retrospective to prevent them from becoming the "new normal."

2.  **Fixed Date (The Commitment):**
    *   **Definition:** Work tied to a non-negotiable external deadline (e.g., a legal filing, a press launch date).
    *   **Flow Impact:** The team must work backward from this date, ensuring all necessary steps are completed *before* the hard stop date.

3.  **Standard (The Bulk of Work):**
    *   **Definition:** The standard, predictable feature work that delivers gradual value. This is where the majority of development capacity should flow.
    *   **Flow Impact:** Managed entirely by WIP limits and smooth flow. The team should aim to finish Standard items at a predictable average rate.

4.  **Intangible / Low Priority:**
    *   **Definition:** Discovery work, research, or "nice-to-have" suggestions.
    *   **Flow Impact:** This work should live primarily in the Backlog and only be pulled through the pipeline when all higher priority WIP limits are cleared, or when the team is deliberately focusing on strategic improvements.

### 🤝 Collaborative Stakeholder Understanding
The process of defining CoS is a core collaborative activity. When a stakeholder submits a request, the team does not accept it blindly. Instead, the team asks:
*"What is the consequence if this feature is delayed by two weeks? Does it stop us from making money? Does it break the law? To determine that, we need to assign it a Class of Service."*

By asking these questions, the team manages expectation and ensures that effort is always directed toward the work that provides the highest, most critical value.

***
**Key Takeaway:** CoS adds a strategic layer to Kanban. It moves the conversation from, *"What do we work on?"* to *"What is the business consequence if we DON'T work on this?"*


