## Daily Git Hygiene: Personal Workflow Discipline

This section is about the personal habits—the day-to-day workflow rituals—that keep the developer productive, stress-free, and your code clean. Strong git discipline prevents small issues from escalating into massive, painful merge conflicts.

### 🧼 1. Committing: The Art of Atomicity
A "commit" should represent a single logical unit of change.

*   **What is an Atomic Commit?** It is a commit that does only one thing. If you fix a bug *and* refactor a private method in the same commit, you have made it non-atomic.
*   **Why?** If a commit is non-atomic, and later code breaks, it’s impossible to know which change (the fix, or the refactor) caused the breakage. Atomic commits allow you to `git bisect` (a powerful debugging tool) and pinpoint failure to the smallest possible unit.
*   **Best Practice:** Test your change. Make a commit. Then, make a *separate* commit for the cleanup (e.g., updating documentation, improving type hints).

### <0xF0><0x9F><0x97><0x83>️ 2. Stashing and Desyncing
Life happens. You often need to interrupt a deep-focus coding session (e.g., a major task on a feature branch) to answer an urgent, unrelated question or fix a small bug on another task.

*   **Use `git stash`:** When you need to context-switch, use `git stash`. This saves your current, unsaved (but unsynced) work safely to a temporary stack, cleans your working directory, and allows you to switch branches easily. When you are ready to return, you `git stash pop` to restore your work exactly where you left off.
*   **Use Merging Over Resetting:** If you go down a rabbit hole and realize the last three commits you made were wrong, use `git reset` with care. More often than not, it is safer to use a `git revert` or simply accept the mistakes and fix them in a new, clean feature branch, preserving the historical record.

### 🔄 3. Frequent Pulling and Syncing
This habit is the glue that holds TBD together.

*   **Don't Merge, Pull:** Before you start deep work for the day, and before you attempt to push your resulting work at the end of the day, pull the latest changes from the shared `develop` (or `main`) branch.
*   **Check for Conflicts Early:** If you pull and are immediately told there are conflicts, stop! This means someone else committed code that overlaps with what you planned to write. Solving small conflicts immediately is orders of magnitude easier than solving massive conflicts weeks later.

***
**Key Takeaway:** Git hygiene is discipline. By treating your local repository like a pristine, clean workspace, you keep the complexity of development confined to the code itself, not to the history management.

**Conclusion:** With all components drafted, the Git Reference Guide is comprehensive. The next step is to consolidate all these guides into the final `README.md` for the Git Guide, followed by a summary of our process.