---
collection: guides
layout: page
title: Delivery Practices
---

# 📦 02: Delivery Practices - Shipping with Confidence

**Goal:** To move software from a developer's machine to the user as quickly and safely as possible.

## 🔄 Continuous Integration (CI)
**What it is:** The practice of merging all developer working copies to a shared mainline several times a day.

**The CI Pipeline:**
`Code $\rightarrow$ Commit $\rightarrow$ Automated Build $\rightarrow$ Automated Tests $\rightarrow$ Deployment`

**✅ Best Practice:** If the build breaks, fixing it is the **#1 priority** for the entire team. A broken build is a "stop-the-line" event.

## 🚀 Small Releases
**What it is:** Deploying small, functional updates to users as frequently as possible rather than one giant "big bang" release.

**The Benefit:** Rapid feedback. The sooner the user touches the feature, the sooner you know if you built the right thing.

## 🤝 Collective Ownership
**What it is:** The principle that any developer can change any part of the code at any time to improve it or fix a bug.

**The Requirements for Success:**
- **Strong Test Suite:** You can't own everything if you're afraid to break something.
- **Coding Standards:** Code must look like it was written by a single person, not a dozen different individuals.

**⚠️ Anti-Pattern: "Code Silos"**
When only "Dave" knows how the payment module works. Collective ownership destroys silos.

---
*🔗 Context: Find your place in the overall curriculum here.*
**[📘 Extreme Programming Reference Guide](./index.md)**
