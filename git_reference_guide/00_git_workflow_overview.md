---
layout: page
title: Git Workflow Overview
---

# Git Best Practices for Agile Teams

This guide provides foundational best practices for managing source code collaboratively in an Agile environment. Git is powerful, but without consistent, clean habits, it can become a source of significant technical debt and friction.

**The Core Philosophy:** The goal of Git hygiene is to ensure that the `main` or `develop` branch is *always* in a healthy, potentially deployable state. We aim for small, frequent, and highly integrated contributions.

---

**Key Principles to Adopt:**

1.  **Always Commit Small and Atomic:** A commit should represent a single, cohesive change. If you fixed a bug and refactored a function—make two separate commits. This makes history readable and acts as a safety net.
2.  **Short-Lived Branches:** Branches should exist for the absolute minimum amount of time required to complete a unit of work. Long-lived branches inevitably drift from the main codebase, creating painful, massive merge conflicts.
3.  **Frequent Integration:** The most vital habit. Do not wait until a feature is "done" to merge. Integrate small bits of working code into the shared development branch *often*. This allows the team to catch integration conflicts hours after they happen, instead of weeks later.

### 🔄 The Integration Paradigm: Moving Toward Continuous Delivery

Instead of rigid silos where developers "own" specific layers (e.g., "only I touch the backend"), we embrace **Continuous Integration**.

**Embracing Vertical Slices**
To avoid merge conflicts, we don't divide work by technical layer; we divide it by **Vertical Slices**. A vertical slice is a small, functional piece of a feature that touches all layers (UI -> API -> Database). By merging these slices quickly, you ensure that no one "owns" a file for too long, and conflicts are handled while they are still small and manageable.

**Collaborative Development: Pairing and Mobbing**
Working on deep vertical slices can be challenging. We encourage:
*   **Pair Programming:** Two developers working on one slice. This allows for immediate peer review and helps juniors navigate complex areas of the codebase without fear.
*   **Mob Programming:** The whole team collaborating on a single complex slice. This is the fastest way to align on architectural decisions and eliminate the "silo" mentality.

**The Workflow Principle:** The main development branch is the current truth. Your goal is to merge your small slice of truth into that truth as quickly as possible. Merge conflicts are not failures—they are **integration signals** telling you that you and a teammate are collaborating on the same area. Handle them early, handle them together.

---
