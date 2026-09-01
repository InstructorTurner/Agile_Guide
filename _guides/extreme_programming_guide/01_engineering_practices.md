---
collection: guides
layout: page
title: Engineering Practices
---

# 🛠️ 01: Engineering Practices - Building Quality In

**Goal:** To introduce the technical habits that prevent bugs and keep the codebase maintainable over the long term.

## 🧪 Test-Driven Development (TDD)
**What it is:** Writing a failing automated test *before* writing the minimum amount of code to make that test pass.

**The Workflow (Red $\rightarrow$ Green $\rightarrow$ Refactor):**
1. **🔴 Red:** Write a small test for a tiny bit of functionality. Run it. It must fail.
2. **🟢 Green:** Write just enough code to make the test pass.
3. **🔵 Refactor:** Clean up the code while keeping the test green.

**✅ Best Practice:** Never write a line of production code without a failing test to justify it.
**⚠️ Anti-Pattern:** Writing all the code first and then "adding tests at the end." This is just testing, not TDD.

## 👥 Pair Programming
**What it is:** Two developers working at one workstation. 
- **The Driver:** Focuses on the tactical task of writing the code.
- **The Navigator:** Focuses on the strategic direction, reviewing the code in real-time, and looking for edge cases.

**✅ Best Practice:** Switch roles frequently. Pairing is not "two people doing one person's job"; it is "two people ensuring the job is done right the first time."

## 🧹 Refactoring
**What it is:** Improving the internal structure of code without changing its external behavior.

**The Rule:** Refactor in small, incremental steps. Never refactor without a safety net of automated tests (like those created via TDD).

## 📐 Simple Design (YAGNI)
**What it is:** Designing the system to meet *current* requirements only. 

**The Golden Rule: YAGNI (You Ain't Gonna Need It)**
Do not add "hooks" or "flexibility" for features you *think* you might need in six months. Build for today; refactor for tomorrow.

---
*🔗 Context: Find your place in the overall curriculum here.*
**[📘 Extreme Programming Reference Guide](./index.md)**
