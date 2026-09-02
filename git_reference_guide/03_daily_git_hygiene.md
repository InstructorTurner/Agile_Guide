---
layout: page
title: Daily Git Hygiene
---

## Daily Git Hygiene: Personal Workflow Discipline

This section is about the personal habits—the day-to-day workflow rituals—that keep the developer productive, stress-free, and your code clean. Strong git discipline prevents small issues from escalating into massive, painful merge conflicts.

### 🧼 1. Committing: The Art of Atomicity
A "commit" should represent a single logical unit of change.

*   **What is an Atomic Commit?** It is a commit that does only one thing. If you fix a bug *and* refactor a private method in the same commit, you have made it non-atomic.
*   **Why?** If a commit is non-atomic, and later code breaks, it’s impossible to know which change (the fix, or the refactor) caused the breakage. Atomic commits allow you to `git bisect` (a powerful debugging tool) and pinpoint failure to the smallest possible unit.
*   **Best Practice:** Test your change. Make a commit. Then, make a *separate* commit for the cleanup (e.g., updating documentation, improving type hints).
### 📦 2. Stashing and Context Switching

Life happens. You often need to interrupt a deep-focus coding session to answer an urgent question or fix a small bug on another task.

*   **Use `git stash` (CLI) or "Stash Changes" (VS Code):** When you need to context-switch, use stashing. This saves your current, unsaved work safely to a temporary stack, cleans your working directory, and allows you to switch branches easily. When you are ready to return, you `pop` your stash to restore your work.
*   **Use Merging Over Resetting:** If you go down a rabbit hole and realize the last three commits you made were wrong, use `git reset` with care. More often than not, it is safer to use a `git revert` or simply accept the mistakes and fix them in a new, clean feature branch, preserving the historical record.

### 🔄 3. The Sync Ritual: Frequent Pulling and Integration

This habit is the glue that holds the Short-Lived Branch model together.

*   **Pull Often, Pull Early:** Do not wait until the end of the day to sync with the team. Pull the latest changes from the shared `develop` branch several times a day.
*   **The Ritual:** 
    1.  Before you start work for the day: `git pull`
    2.  Before you start a new slice: `git pull`
    3.  Before you open a PR: `git pull`
*   **Check for Conflicts Early:** If you pull and see conflicts, stop! This is your **integration signal**. It means a teammate is working in the same area. Solving a 2-line conflict now is orders of magnitude easier than solving a 200-line conflict on Friday afternoon.

***

**Key Takeaway:** Git hygiene is discipline. By treating your local repository like a pristine, clean workspace, you keep the complexity of development confined to the code itself, not to the history management.
