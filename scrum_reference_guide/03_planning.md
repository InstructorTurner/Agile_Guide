---
layout: page
title: Planning
---

# 🗓️ 03: Sprint Planning - Defining the Mission

**Goal:** To ensure the whole team understands the objective and commits to a defined, achievable set of work for the upcoming timebox (the Sprint).

## ⚙️ What is a Sprint?
A Sprint is the heartbeat of Scrum. It is a short, fixed period (usually 1-4 weeks) during which the team works to realize a desirable outcome. All events leading up to, and including, the Sprint must fit within this timebox.

## 🚀 The Purpose of Sprint Planning
Sprint Planning is the meeting where we take the top-priority items from the Product Backlog and agree on *what* we will build and *how* we will build it during the next Sprint.

**Inputs to the Meeting:**
1. **The Product Backlog:** (The list of all potential work, prioritized)
2. **The Team Capacity:** (How many people are available, and for how long?)
3. **The Shared Goal:** (What is the biggest piece of value we can deliver in this timeframe?)

**Outputs of the Meeting:**

1. **The Sprint Goal:** A clear, concise, and motivating statement describing the *purpose* of the current Sprint. (E.g., "Allow registered users to view their order history.")
    *   *Why is this critical?* The Goal keeps the team focused and prevents scope creep mid-sprint.
2. **The Sprint Backlog:** The set of User Stories and tasks the team commits to completing in this Sprint. This is the detailed plan.

**💡 For those with Waterfall experience:** Think of the Sprint Backlog as a **forecast**, not a rigid contract. While we commit to the *Goal*, the specific tasks used to get there may evolve as we discover more during the Sprint.

### ⚠️ Mini-Warning: Protecting the Sprint Backlog
Once the Sprint Planning is complete and the Sprint Goal is set, the scope is highly protected. Adding major, unplanned features during the Sprint requires renegotiation with the Product Owner and consensus from the entire team.

## 📖 Narrative Example: From Product Backlog to Sprint Backlog

Imagine the team is entering Planning for a 2-week Sprint.

### Step 1: Defining the Goal (The "Why")
The Product Owner (PO) presents the top of the Product Backlog, which includes "Payment Integration," "User Profile Edits," and "Password Reset."

Instead of just grabbing the top three items, the team discusses the biggest immediate value. They agree on a **Sprint Goal**: *"Enable users to complete a purchase securely."*

Because of this goal, they pull in "Payment Integration" and "Order Confirmation Email," but they decide to leave "User Profile Edits" for the next sprint, even though it's high priority, because it doesn't support the current mission.

### Step 2: Building the Sprint Backlog (The "How")
Now the team looks at the "Payment Integration" story. To ensure they maintain **vertical slices** (delivering a working piece of functionality from DB to UI), they break the story into implementation steps rather than architectural layers:

*   **Story:** "As a customer, I want to pay via Credit Card so I can complete my order."
    *   **Task 1:** Implement basic credit card payment flow (DB -> API -> UI)
    *   **Task 2:** Implement payment validation and error handling (DB -> API -> UI)
    *   **Task 3:** Implement payment success confirmation screen (DB -> API -> UI)

**Result:** The team doesn't just "finish the database work"; they deliver a series of small, working increments that move them toward the Sprint Goal.

---
*🔗 Context: Find your place in the overall curriculum here.*
**[📘 Scrum Fundamentals Reference Guide](./index.md)**
