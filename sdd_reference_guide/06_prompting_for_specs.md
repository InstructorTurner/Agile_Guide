# 06 Prompting for Specs

[← Back to Index](index.md)

Once you have your hand-written breakdown and have refined it through conversation, you need to turn that "messy" human thought process into a structured specification that an agent can execute reliably.

## The Anatomy of a Great Spec

An agent-ready specification should be **unambiguous, structured, and bounded**. Avoid words like "efficient," "modern," or "intuitive"—these are vibes, not specifications.

### Key Elements
- **User Stories**: "As a [user], I want to [action] so that [value]."
- **Functional Requirements**: Precise descriptions of behavior.
  - *Bad*: "The app should load photos quickly."
  - *Good*: "The app should render the first 20 photos within 200ms of the album being opened."
- **Constraints**: Technical or business limits.
  - *Example*: "Data must be stored in a local SQLite database; no external cloud storage."
- **Success Criteria**: How do we know it's done?
  - *Example*: "A user can create an album, add three photos, and see the album sorted by the date the photos were taken."

## From Breakdown to Spec: The Prompt

When asking an agent to generate the final spec from your breakdown, use a **structural prompt**.

### Example Prompt
> "I have a hand-written breakdown for a photo album feature. I want you to turn this into a formal Technical Specification. 
> 
> Please organize it into the following sections:
> 1. **Core Objective** (One sentence)
> 2. **User Stories** (Bullet points)
> 3. **Functional Requirements** (Numbered list)
> 4. **Technical Constraints** (Bullet points)
> 5. **Definition of Done** (Checklist)
> 
> Here is my breakdown: [Insert your notes here]"

By defining the structure, you prevent the AI from omitting critical sections and ensure the output is in a format that can be easily tracked during the iteration cycle.
