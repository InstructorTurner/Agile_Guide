# 02 Fighting Automation Blindness

[← Back to Index](index.md)

Automation Blindness is the psychological phenomenon where a developer stops critically analyzing output because the tool producing it is generally reliable. 

## The "Polished Output" Trap

AI agents generate code and documentation that is syntactically perfect and professionally formatted. This "veneer of correctness" can trick your brain into skipping the validation step. You see a clean function with a docstring and a few tests, and you assume it works.

### Symptoms of Automation Blindness
- **The "LGTM" Reflex**: Clicking "Accept" or "Merge" on a large diff without being able to explain exactly how the logic works.
- **Implicit Trust**: Assuming the AI handled an edge case (like null values or network timeouts) because it "usually does."
- **Requirement Drift**: Accepting a feature that works but slightly changes the original intent of the product because the AI's implementation was "easier" to generate.

## Strategies for Staying Sharp

To fight automation blindness, adopt a **skeptical mindset**:

1. **The "Explain it to Me" Test**: Before accepting a block of code, ask yourself: *"Could I explain exactly why the AI chose this specific approach over another?"* If the answer is no, you are experiencing automation blindness.
2. **Intent Validation**: Compare the generated code not against the AI's summary, but against your **original hand-written breakdown**. 
3. **Assume Failure**: Start with the assumption that the AI has missed one critical edge case. Actively hunt for that missing piece rather than waiting for a bug report.
