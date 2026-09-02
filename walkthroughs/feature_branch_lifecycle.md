# 🌿 Feature Branch Lifecycle: From Work Item to Dev

Your mission is to take a task from a Work Item in Azure DevOps to a successfully integrated piece of code in the `dev` branch, maintaining a clean and professional git history.

## 🎯 Final Deliverable
1. A feature successfully merged into the `dev` branch via Azure DevOps.
2. A clean local environment with the feature branch deleted.
3. A PR history that shows you resolved conflicts locally before requesting reviews.

---

## 🛠️ The Workflow

### Phase 1: Initiation (The Setup)
Never start a feature from a stale codebase. Always synchronize with the team's current truth first.

- **Naming Convention:** Use the format `feature/WorkItemID-short-description`.
  - *Example:* `feature/456-user-login`
- **The Starting Point:**
  1. `git checkout dev` -> Switch to the integration branch.
  2. `git pull` -> Get the latest changes from the team.
  3. `git checkout -b feature/456-user-login` -> Create your isolated workspace.

### Phase 2: The Iterative Loop (Development)
Follow the "Small and Atomic" principle. Huge commits are hard to review and dangerous to revert.

- **Commit Often:** Every time you complete a small, logical piece of the task, commit it.
- **Vertical Slicing:** Focus on delivering a small, working piece of functionality (UI -> API -> DB) rather than building all the DB work first and the UI last.

### Phase 3: The Integration Sync (The "Dev Merge")
Avoid "Merge Conflict Shock" during the PR process. Resolve conflicts locally on your own time, not during the review.

- **The Habit:** Before opening your PR in Azure DevOps, bring the latest `dev` changes into your branch.
- **The Workflow:**
  1. `git checkout dev` -> Switch to dev.
  2. `git pull` -> Get latest updates.
  3. `git checkout feature/456-user-login` -> Return to your feature.
  4. `git merge dev` -> Integrate the team's work into your branch.
- **Conflict Resolution:** If conflicts occur, use your editor to resolve them, then commit the result.

### Phase 4: The Peer Review (The ADO PR)
The Pull Request is a conversation about quality, not a hurdle to jump over.

- **Submission:** Create the PR in Azure DevOps and link it to the corresponding Work Item.
- **The Goal:** Secure **2 peer approvals**. 
- **Addressing Feedback:** When a reviewer suggests a change, make the edit locally, commit it, and push to the same branch. The PR will update automatically.

### Phase 5: The Integration & Cleanup (The Finish)
A professional developer leaves the campsite cleaner than they found it.

- **The Merge:** Complete the **Merge Commit** into `dev` via the Azure DevOps interface.
- **The Housekeeping:**
  1. `git checkout dev` -> Return to the integration branch.
  2. `git pull` -> Pull your merged feature (and others' work) down to your machine.
  3. `git branch -d feature/456-user-login` -> Delete the local branch to keep your workspace tidy.

---

## ✅ Git Hygiene Checklist
Before you consider the task "Done," audit your process:

- [ ] Did I start my branch from the latest `dev`?
- [ ] Does my branch name follow the `feature/WorkItemID-desc` convention?
- [ ] Did I merge `dev` into my branch to resolve conflicts *before* opening the PR?
- [ ] Did I get 2 peer approvals in Azure DevOps?
- [ ] Did I delete my local branch after the merge?
