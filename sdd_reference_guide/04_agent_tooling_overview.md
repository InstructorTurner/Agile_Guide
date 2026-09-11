# 04 Agent Tooling Overview

[← Back to Index](index.md)

To implement Spec-Driven Development, you need tools that can move beyond simple chat interfaces and interact directly with your codebase. These are known as **AI Coding Agents**.

## Chatbots vs. Agents

It is important to distinguish between a standard AI chatbot and an agent:

| Feature | Chatbot (e.g., standard ChatGPT/Claude) | Agent (e.g., Pi, OpenCode) |
| :--- | :--- | :--- |
| **Scope** | Limited to the chat window | Access to the local file system |
| **Action** | Suggests code for you to copy/paste | Can create, read, and edit files directly |
| **Context** | Limited by the prompt window | Can index the codebase to find relevant files |
| **Execution** | Cannot run commands | Can run bash commands, tests, and linters |

## Choosing Your Primary Agent

Depending on your project and preferred level of control, you will likely choose one of these as your primary coding agent.

### Pi: The Lightweight Agent
Pi is a flexible, conversation-centric agent. It is ideal for developers who prefer a leaner experience.

**Benefits:**
- **Low Context Usage**: Pi generally consumes fewer tokens, making it faster and less prone to "forgetting" early parts of the conversation.
- **Easy Self-Extensibility**: You can easily shape Pi's behavior through custom instructions and high-level guidance.
- **Conversational Depth**: Its strengths lie in the exploration and refinement phase of SDD.

**Drawbacks:**
- **No Built-in Planning Mode**: Pi does not have a native, structured "planning" state; you must manually enforce the SDD structure.
- **Limited Toolset**: Compared to full CLI agents, Pi has fewer built-in tools for automated file management and execution.

### OpenCode: The Heavy-Duty Agent
OpenCode is a powerful CLI-based agent designed for deep integration with your development environment.

**Benefits:**
- **Structured Planning**: Built-in support for complex planning and execution workflows.
- **Deep System Integration**: Extensive capabilities for reading, writing, and executing code across a large codebase.
- **Robust Tooling**: Access to a wider array of agentic tools, making it highly effective for the "Convergence" phase of SDD.

**Drawbacks:**
- **High Context Usage**: Its powerful indexing and tool-use can consume more context, potentially leading to higher costs or limited window size.
- **Complexity**: Steeper learning curve for initial configuration and optimal usage.

## Which one should you use?

- **Use Pi if**: You are working on a small script, a rapid prototype, or you prefer to manually architect every step of the planning process.
- **Use OpenCode if**: You are building a full-scale application, performing complex refactors, or utilizing `spec-kit` to automate the convergence of your code against a formal spec.

