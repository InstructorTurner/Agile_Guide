# 08 Speckit Core Workflow

[← Back to Index](index.md)

The power of Spec Kit lies in its structured, multi-step workflow. It prevents the "one-shot" fallacy by forcing the agent to move through distinct phases of development.

## The Golden Path

Follow these slash commands in order to build a feature from scratch:

### 1. Define the Intent (`/speckit.specify`)
Describe **what** you want to build and **why**. Focus on the requirements and user stories. 
*Avoid talking about the tech stack here; focus entirely on the behavior.*

### 2. Create the Technical Plan (`/speckit.plan`)
Now, define **how** to build it. This is where you specify the tech stack, architecture, and library choices. 
*Example: "Use Vite with vanilla JS and a local SQLite database."*

### 3. Generate Actionable Tasks (`/speckit.tasks`)
The agent breaks the plan down into a granular, checklist-style task list. This turns a high-level plan into a series of small, verifiable steps.

### 4. Execute Implementation (`/speckit.implement`)
The agent executes the tasks in order, writing the code to satisfy the spec and the plan.

### 5. Converge (`/speckit.converge`)
This is the most critical step. The agent assesses the resulting codebase against the original spec, plan, and task list. 
- If gaps are found, the agent appends new tasks to the list.
- You repeat the **Implement -> Converge** loop until the agent reports that the project has **Converged**.

## Why This Sequence Matters

By separating **Specify -> Plan -> Tasks -> Implement**, you create a series of "check-gates." If the implementation is wrong, you can easily identify if the error happened because:
- The **Spec** was ambiguous.
- The **Plan** was flawed.
- The **Tasks** were incomplete.
- The **Implementation** just had a bug.
