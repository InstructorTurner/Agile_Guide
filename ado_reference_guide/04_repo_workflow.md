---
layout: page
title: Repo Workflow
---

# 🛠️ Repo Workflow

Azure Repos is where our code lives. The most important part of the repo workflow for a junior developer is the link between the code and the planning boards.

## The Golden Rule: Link Your Work

Never submit a Pull Request (PR) that isn't linked to a Work Item. This provides "traceability"—anyone looking at the code in six months can see exactly which User Story required that change.

## The Standard Workflow

### 1. Creating a Branch
When you start a task, create a new branch. 

*   **ADO Tip**: In **Repos > Branches**, when creating a new branch, you can search for and select the associated Work Item. ADO will often suggest a branch name based on the work item ID (e.g., `userstory-123-login-validation`).

### 2. Submitting a Pull Request (PR)
Once your code is complete and tested:
1.  Navigate to **Repos > Pull Requests**.
2.  Click **New Pull Request**.
3.  **Link the Work Item**: In the right-hand sidebar, use the "Work Items to link" section to add the Story or Task you completed.
4.  **Assign Reviewers**: Add your teammates to the PR for feedback.

## 🛠️ ADO Repo Features for Juniors

*   **Files View**: Use the **Repos > Files** menu to explore the codebase. You can click on any file to see its history or jump to a specific commit.
*   **PR Comments**: Use the comment feature in PRs to ask questions about a specific line of code. Instead of a general "this is wrong," use "Could you explain why we chose this approach here?"

## 💡 Narrative Example: The Mystery Commit

Imagine a bug is discovered in production. The lead developer looks at the code and sees a change made three months ago. Because you linked your PR to a Work Item, they can click the link and immediately find the original User Story: "Fix edge case for international phone numbers."

Without that link, the commit is a "mystery commit," and the lead would have to spend an hour guessing why the change was made.
