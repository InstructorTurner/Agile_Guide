---
layout: page
title: Backlog Management
---

# 02: Product Backlog Management - Prioritizing Value

**Goal:** To define the Product Backlog as the single, authoritative source for *all* desired features and improvements for the product.

## 📑 What is the Product Backlog?
Think of the Product Backlog as the **Master Wishlist**—but one that is constantly managed, prioritized, and refined by the Product Owner and the team.

*   **Definition:** A single, ordered list of everything that might be needed in the product.
*   **Ownership:** The **Product Owner (PO)** owns the backlog, meaning they are accountable for its content, business value, and prioritization.
*   **Nature:** It is a *living document*. It is never finished.

### 📈 How is the Backlog Prioritized?
The items must be prioritized because we cannot build everything at once! Prioritization is not just about 'who yells the loudest.' Key factors include:

1.  **Business Value:** How much revenue or competitive edge does this feature provide? (Highest value gets highest priority.)
2.  **Risk/Dependency:** Does this feature unlock several other features? If it's foundational technical work (like setting up a service), it might be prioritized high, even if the user benefit isn't immediately visible.
3.  **Effort/Dependencies:** Can we group small, low-effort stories together to deliver a slice of value quickly?

### ♻️ Backlog Refinement (Grooming)
Refinement is the ongoing process where the development team and the Product Owner meet to review items at the top of the backlog.

**Goal of Refinement:** To take vague ideas and turn them into well-understood, ready-to-implement User Stories.

During refinement, we focus on:
*   **Elaboration:** Adding enough detail to the User Stories so that a developer can start working without needing immediate clarification.
*   **Sizing:** The team estimates the story's **size** (using methods like Story Points) to gauge complexity and estimate effort.
    *   **Why Story Points?** We use *relative sizing* (e.g., "This is a 3, and that is a 5") instead of hours because humans are poor at estimating exact time but great at comparing size. It accounts for uncertainty and complexity without the pressure of a rigid hourly deadline.
*   **Splitting/Decomposition:** If a story is too large (it requires too many resources or takes longer than a sprint), the team immediately works to split it into smaller, INVEST-compliant stories.

## 📖 Narrative Examples

### Example 1: The Evolution of a Feature (Epic -> Story)
To see how the backlog transforms from a "wishlist" to "ready" work, follow the evolution of a single feature:

1.  **Initial Idea (The "Wish"):** "We need user profiles." (Too vague, stays at the bottom of the backlog).
2.  **Refined Epic (The "Goal"):** "As a registered user, I want to manage my profile information so that my account details remain current." (Better, but still too large for one sprint).
3.  **Split Stories (The "Execution"):** The team splits the Epic into smaller, deliverable slices:
    *   *Story A:* "As a user, I want to upload a profile picture." (Estimated: 3 points)
    *   *Story B:* "As a user, I want to edit my email and password." (Estimated: 5 points)
    *   *Story C:* "As a user, I want to set my notification preferences." (Estimated: 2 points)

**Result:** The PO can now prioritize Story B (critical for security) over Story A (cosmetic), delivering value faster.

### Example 2: A Refinement Session in Action
Imagine a conversation between a Product Owner (PO) and the Development Team:

**PO:** "Next up is 'Implement Social Login.' I want users to be able to sign in with Google or GitHub."
**Dev:** "Is this just for new accounts, or should existing users be able to link their accounts too?" (**Elaboration**)
**PO:** "Great point. Let's start with just new accounts for the MVP."
**Dev:** "Even for just new accounts, doing both Google and GitHub might be too much for one sprint. Let's split these into two separate stories." (**Splitting**)
**PO:** "Agreed. Let's do Google first."
**Dev:** "Compared to the Email Login we did last month (which was a 3), Google Login feels slightly more complex due to the OAuth setup. Let's call this a 5." (**Sizing**)


---
*🔗 Context: Find your place in the overall curriculum here.*
**[📘 Scrum Fundamentals Reference Guide](./index.md)**
