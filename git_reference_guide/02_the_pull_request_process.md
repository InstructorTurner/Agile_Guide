---
layout: page
title: The Pull Request Process
---

## Best Practices for Code Review and Validation

The Pull Request (PR) submission and review cycle is the technical manifestation of the Agile principle: **Collective Code Ownership.** Every developer's code is reviewed by the team, and every review strengthens the entire team.

### 🤝 The Reviewer's Code of Honor: Anti-Rubber-Stamping

An approval is not a checkbox; it is a shared commitment. When you approve a PR, you are stating: *"I have read this code, I understand how it works, and I am equally responsible for any bugs it introduces."*

**Rubber-stamping (approving without thorough review) is a failure of collective ownership.** It creates a false sense of security and allows technical debt to seep into the `develop` branch.

**How to avoid rubber-stamping:**
*   **Actually run the code:** If the change is significant, pull the branch locally and test it.
*   **Challenge the logic:** Don't just look for syntax errors; ask, *"Why was it done this way? Is there a simpler approach?"*
*   **Verify the tests:** Ensure the tests actually test the logic, not just the "happy path."

### 👁️ Crafting a Review: The High-Value Reviewer

The best reviewers are those who don't just report bugs, but who actively seek out areas of theoretical risk and missed dependencies.

**1. The Three 'Lenses' Approach:** When reviewing code, systematically check the following three areas:
    *   **Logical Integrity:** Does the code solve the right problem? Does it introduce bugs? (Focus on *what* it does).
    *   **Architectural Fit:** Does it honor the system's existing structure? Is this the best place for this logic? (Focus on *where* it lives).
    *   **Maintainability:** Is it clear? Is it easy to read? Is the naming convention consistent? (Focus on *how* it is written).

**2. Giving Constructive Feedback:** Never treat a review as an interrogation. Always make suggested improvements constructive and explain the *why*.
    *   **Bad Feedback:** "This function is too long. Break it up."
    *   **Good Feedback:** "This function is doing three distinct things: fetching data, sanitizing it, and then calling the API. I suggest breaking it into three steps—`fetchData()`, `sanitizeData()`, and `callAPI()`—because it improves readability and allows us to test these steps in isolation."

**3. The Testing Mindset in Review:** Never assume the developer tested everything. A good review involves reviewing the *tests* alongside the code:
    *   **Identify Missing Paths:** If the code handles a successful path, the review should check if the corresponding unit test explicitly validates a failure path (e.g., what happens if the API returns a 404 error?).
    *   **Test Coverage:** Ensure that the new code has sufficient test coverage to prevent regressions.

### ⚡ Keeping the Cycle Fast

To ensure that high-frequency integration remains possible, we must keep the PR cycle short.

*   **Keep PRs Small:** It is significantly easier and faster to review 5 small PRs than one massive PR. Small PRs are reviewed more thoroughly and merged faster.
*   **Prompt Reviews:** Treat reviewing as a primary task, not an interruption. Aim to review peer PRs within a day of submission.
*   **Collaborative Resolution:** If a PR has more than 3-4 conflicting comments, stop typing and start talking. Hop on a quick call or pair up in person to resolve the issue immediately.

### 🤝 Collaborative Ownership (The Stakeholder Model)
The act of reviewing forces the reviewer to adopt the *user's* point of view, a skill essential to Agile. By arguing the merits of the code, the reviewer is practicing the mindset of the QA engineer, the architect, and the ultimate user—all skills vital to the collective success of the team.

---
**Key Takeaway:** A review is a paid opportunity to teach. If you learn something new about the codebase while reviewing, credit that knowledge transfer!