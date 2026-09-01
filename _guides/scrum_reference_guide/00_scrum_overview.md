---
collection: guides
layout: page
title: Scrum Overview
---

# 🧭 00: Scrum Overview - The Foundation

**Goal:** To provide a clear, jargon-free understanding of what Scrum is, what Agile means, and the mindset we need to adopt as a development team.

## 🧐 What is Agile?
Agile is not a specific process; it's a **mindset**. It's an approach that values adaptability, collaboration, and the early and continuous delivery of working software over rigid, up-front planning.

**Old Way (Waterfall):** Build everything, test everything, show the client at the end. (High risk, low feedback.)
**New Way (Agile/Scrum):** Build, test, show a small bit, get feedback, adjust, repeat. (Low risk, continuous improvement.)

## ⚛️ What is Scrum?
Scrum is the *framework* (the set of rules and roles) we use to implement the Agile mindset. It provides the structure for our sprints and events.

### Key Concepts to Know:

*   **Scrum Team:** We are a small, self-managing team responsible for all aspects of the product (design, development, testing, etc.).
*   **Iterative:** We work in short, time-boxed cycles (Sprints) rather than long, continuous cycles.
*   **Empiricism:** Our work is based on *observation* and *experimentation*. We don't assume; we build, measure, and learn.

### 🚧 Foundational Best Practices (Mindset Rules)

#### 🛑 Anti-Pattern Alert 1: Limiting Work In Progress (WIP)
**Problem:** Trying to work on too many features or tasks at once. This is like spreading yourself too thin—nothing gets done efficiently.
**Rule:** Only pull tasks into active development only when the previous task is **done**. Focus on finishing a small set of items (e.g., 3-5 user stories) completely before starting anything new.

#### ✅ Best Practice: Building Vertical Slices
**Problem:** Developing a full layer of code horizontally (e.g., finishing all the database setup, then all the backend logic, then all the front-end styling). This leads to large, untested chunks of code that don't prove end-to-end value.

**Rule:** When tackling a feature, focus on delivering a **Vertical Slice**.
*   **Definition:** A vertical slice is a minimal, end-to-end package that takes a feature from the user interface, through the necessary business logic, and into the database.
*   **Benefit:** This proves that the feature works *in the hands of a user* and provides immediate, tangible value that stakeholders can see and test.

#### 🤝 Collaboration: Pairing and Swarming
Scrum is a team sport. We don't just divide tickets and work in silos; we collaborate to get things "Done."
*   **Pairing:** Two developers working on one task at one workstation. This improves quality, spreads knowledge, and reduces bugs.
*   **Swarming:** When the team focuses multiple people on a single high-priority story to push it across the finish line. It is better to have one story "Done" than five stories "almost done."

---
*🔗 Context: Find your place in the overall curriculum here.*
**[📘 Scrum Fundamentals Reference Guide](./index.md)**
