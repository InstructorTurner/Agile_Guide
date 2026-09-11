# 03 Conversational AI Workflow

[← Back to Index](index.md)

Most developers use AI as a "vending machine": *Prompt -> Code*. To succeed in Spec-Driven Development, you must treat the AI as a **collaborator** and a **sounding board**.

## Shift: From Execution to Exploration

Instead of asking the AI to implement, use the initial phase of the conversation to refine the specification.

### The "Question-First" Approach

Before moving to implementation, push the AI to challenge your assumptions. Use prompts like:
- *"Here is my breakdown. What edge cases have I missed?"*
- *"Are there any contradictions in these requirements?"*
- *"If you were to implement this, where would you expect the most complexity or risk?"*
- *"Can you suggest three different ways to structure this data, and explain the trade-offs of each?"*

## The Refinement Loop

The goal is to reach a state of **Shared Understanding** before any code is written.

1. **Present**: Give the AI your hand-written breakdown.
2. **Challenge**: Ask the AI to find gaps or suggest improvements.
3. **Revise**: Update your breakdown based on the conversation.
4. **Confirm**: Explicitly state: *"We have agreed on X, Y, and Z. This is now our final spec."*

## Why This Works

By forcing the AI to ask questions and suggest revisions, you are effectively using the LLM's vast training data to uncover "unknown unknowns." This process ensures that when you finally move to implementation, the AI isn't guessing—it's executing a validated plan.
