---
layout: page
title: User Story Guide
---

# 🧩 01: User Story Guides - Defining the Value

**Goal:** To explain what a User Story is, how to write high-quality ones, and critically, how to structure them to enforce 'vertical slices.'

## 📖 What is a User Story?
A User Story is a simple, non-technical description of a feature written from the perspective of the end-user. It captures *value* rather than just technical tasks.

**Crucial Mindset:** A User Story is not a detailed requirement document—it is a **placeholder for a conversation**. The real detail emerges through discussion between the developer, the Product Owner, and the stakeholders.

**The Standard Format:**
> "As a [Type of User], I want to [Goal], so that [Reason/Benefit]."

*   **Example (Bad):** "Implement database connection." (Too technical, no value.)
*   **Example (Good):** "As a **registered user**, I want to **reset my password via email**, so that **I can regain access to my account**." (Clear value, clear user.)

## 📐 The Anatomy of a Good Story
A good User Story must be:

1.  **INVEST:**
    *   **I**ndependent: Can be worked on in isolation?
    *   **N**egotiable: Does it have defined acceptance criteria? (Yes, but flexible enough for discussion.)
    *   **V**aluable: Does it deliver tangible user value? (Must do.)
    *   **E**stimable: Can the team size up the effort?
    *   **S**mall: Can it be completed within a single sprint?
    *   **T**estable: Can we write automated tests for it?

2.  **Acceptance Criteria (AC):** These are the specific, testable conditions that must be met for the story to be considered "Done." They clarify the story's boundaries.
    *   **Example Story:** Reset Password
    *   **AC 1:** The user must receive a unique reset link within 60 seconds of requesting it.
    *   **AC 2:** The link must expire after 24 hours.
    *   **AC 3:** Multiple failed login attempts must be blocked for 15 minutes.

### ⚠️ Anti-Pattern Alert 2: Focusing on Vertical Slices
**The Trap:** Writing user stories that require too many components to work together immediately, thus becoming huge and spanning multiple sprints.
**How to Fix It:** Break the story down into several small, independent, valuable micro-stories.

| Instead of this HUGE Story (The Anti-Pattern) | Break it into these Small, Vertical Slices (The Solution) |
| :--- | :--- |
| "Implement the entire user authentication flow (login, signup, password reset)." | 1. **Signup:** "As a new user, I can create an account with valid email/password." |
| | 2. **Login:** "As a registered user, I can log in with my credentials." |
| | 3. **Password Reset:** "As a user, I can initiate a password reset via my email." |

By keeping each slice small, we deliver functional value faster and reduce risk.

---
*🔗 Context: Find your place in the overall curriculum here.*
**[📘 Scrum Fundamentals Reference Guide](./index.md)**
