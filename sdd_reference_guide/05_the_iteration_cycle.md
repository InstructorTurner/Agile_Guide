# 05 The Iteration Cycle

[← Back to Index](index.md)

In SDD, the "first pass" of code is rarely the final pass. The magic happens in the iteration cycle—the process of refining the implementation against the specification.

## The SDD Loop

The iteration cycle is not about "fixing bugs," but about **converging** the implementation with the intent.

1. **The Spec Check**: Run the agent's output against your original spec. Does it actually do what you asked, or did it take a "shortcut" that violates the intent?
2. **The Gap Analysis**: Identify exactly where the code diverges from the spec. 
    - *Example*: "The spec requires the photo albums to be groupable by date, but the implementation currently only sorts them alphabetically."
3. **The Targeted Refinement**: Instead of saying "fix it," provide the agent with the specific gap.
    - *Prompt*: "In `album_manager.ts`, the sorting logic is using `alphaSort`. Please update this to `dateSort` as per requirement #3 of the spec."
4. **Verification**: Confirm the fix and ensure no regressions were introduced.

## Handling "Brownfield" Changes

"Brownfield" development is when you change a specification for a feature that has already been implemented. This is where most developers fail by simply prompting the AI to "change this one thing."

**The correct Brownfield Loop:**
1. **Update the Spec First**: Modify your specification document to reflect the new requirement.
2. **Re-Plan**: Ask the agent to create a new implementation plan based on the updated spec.
3. **Converge**: Implement the changes and verify that the codebase now matches the *new* spec.

By updating the spec first, you ensure that your documentation doesn't rot and that the AI has a stable anchor for its changes.
