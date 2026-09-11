# 00 Introduction to SDD

[← Back to Index](index.md)

Spec-Driven Development (SDD) is a software development methodology that flips the traditional relationship between specifications and code. 

## The Core Shift

In traditional development, a spec is often a static document that guides the developer, but is frequently discarded or ignored once coding begins. In SDD, the **specification is the source of truth**. 

Instead of jumping from a vague idea directly to code, SDD introduces a structured layer of intent:
1. **Intent (The "What" and "Why")**
2. **Specification (Structured Requirements)**
3. **Plan (Technical Approach)**
4. **Implementation (The Code)**

## Why SDD for AI-Native Development?

When working with LLMs, the biggest risk is the "one-shot" fallacy: the belief that a single perfect prompt can generate a perfect feature. This leads to "vibe-coding," where the developer accepts code that *looks* right but fails to meet deep architectural needs.

SDD provides the guardrails needed to ensure that:
- The developer remains the architect.
- The AI remains the implementer.
- The requirements are validated *before* they are encoded.

By focusing on the specification first, you ensure that the AI is building exactly what you need, rather than what it *guesses* you need.
