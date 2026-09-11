# 09 Speckit Advanced Tools

[← Back to Index](index.md)

Beyond the core workflow, Spec Kit provides extensions and presets to handle complex real-world scenarios like bug fixing and organizational standardization.

## Extensions: Adding New Capabilities

Extensions add entirely new commands to your agent. One of the most powerful bundled extensions is the **Bug Extension**.

### The Bug Fix Workflow
Bug fixing with AI is risky because agents often jump straight to a patch without understanding the root cause. The bug extension enforces a disciplined flow:

1. `/speckit-bug-assess "<bug report>" slug=bug-name`
   - The agent investigates the code to find the root cause.
2. `/speckit-bug-fix slug=bug-name`
   - The agent implements a targeted fix based on the assessment.
3. `/speckit-bug-test slug=bug-name`
   - The agent verifies the fix against the original symptom.

## Presets: Customizing the "How"

While extensions add *new* tools, **Presets** change how existing tools behave. 

Presets allow you to enforce organizational standards without writing new prompts for every project. For example, a "Security Preset" might:
- Update the `/speckit.plan` template to require a security review step.
- Update the `/speckit.specify` template to require a "Data Privacy" section.

## Bundles: Role-Based Setups

Bundles are collections of extensions and presets tailored to specific roles. Instead of installing five different extensions, you can install a single bundle:

```bash
specify bundle install developer
```

This ensures that every developer on a team has the same set of tools and follows the same SDD standards.
