---
layout: page
title: Work Item Hierarchy
---

# 📦 Work Item Hierarchy

In ADO, we use a structured hierarchy to organize work. This prevents "big" ideas from becoming overwhelming and ensures that every line of code can be traced back to a business goal.

## The Hierarchy Levels

We follow a top-down approach: **Epics** -> **Features** -> **User Stories** -> **Tasks**.

### 1. Epics
The highest level of organization. Epics represent large business initiatives that typically span multiple sprints or even months.

*Example:* "Modernize User Authentication System."

### 2. Features
Epics are broken down into Features. A Feature is a deliverable piece of functionality that provides value to the user but is too large to fit into a single sprint.

*Example:* "Implement Multi-Factor Authentication (MFA)."

### 3. User Stories
Features are broken down into User Stories. A story is the smallest unit of "value." It should be small enough to be completed within a single sprint.

*Example:* "As a user, I want to receive a SMS code during login so that my account is secure."

### 4. Tasks
User Stories are broken down into Tasks. Tasks are the technical steps required to complete the story. These are for the developers' eyes and describe the actual work.

*Example:* "Create database table for MFA tokens" or "Integrate with Twilio API."

### 5. Bugs
Bugs are used to track when something that was previously working is now broken, or when a delivered feature doesn't meet the acceptance criteria. Unlike Stories, Bugs represent "corrective" work rather than "new" value.

*Example:* "Login page crashes when entering a special character in the password field."

## 🛠️ How to Navigate and Manage Relationships in ADO

### Viewing Relationships
To see this relationship, go to **Boards > Backlogs**. 

In the top right corner, you can toggle the view between Epics, Features, and Backlog items (Stories). When you enable the **Parents** view in the column options, you can see exactly which Feature your story belongs to and which Epic that Feature supports.

### Creating Child Items
If you identify a new task or story that belongs under an existing item, you can create it as a child:

1.  Open the "Parent" work item.
2.  Look for the **Related Work** section in the right-hand sidebar.
3.  Click **Add link** and select **New item**.
4.  Choose the type of child (e.g., if you are in a Story, you would create a **Task**).

This automatically creates the link, ensuring the hierarchy remains intact.


## 💡 Narrative Example: The Traceability Chain

If a senior developer asks you *why* you are creating a specific database table, you can trace it back:
* Your **Task** is "Create MFA Token Table."
* This is part of the **User Story** "SMS Code Login."
* Which is part of the **Feature** "Implement MFA."
* Which is part of the **Epic** "Modernize User Authentication."

This ensures we aren't building things "just because," but are always contributing to a larger goal.
