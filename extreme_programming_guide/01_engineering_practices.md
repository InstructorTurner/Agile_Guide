# Engineering Practices

These practices focus on the technical quality of the code and the process of writing it.

## Test-Driven Development (TDD)
**What it is**: Writing a failing automated test *before* writing the minimum amount of code to make that test pass.
**Best Practice**: Red $\rightarrow$ Green $\rightarrow$ Refactor.
**Scrum Integration**: Use TDD during the "Development" phase of a Sprint task to ensure the "Definition of Done" is met with verifiable quality.

## Pair Programming
**What it is**: Two developers working at one workstation. One writes code (Driver), while the other reviews and thinks strategically (Navigator).
**Best Practice**: Switch roles frequently.
**Scrum Integration**: Pair on complex User Stories to reduce bugs and spread knowledge across the team, reducing "key person" dependencies.

## Refactoring
**What it is**: Improving the internal structure of code without changing its external behavior.
**Best Practice**: Refactor in small steps; never refactor without a safety net of tests.
**Scrum Integration**: Allocate time for refactoring as part of every Story, rather than creating separate "technical debt" tickets.

## Simple Design
**What it is**: Designing the system to meet current requirements without over-engineering for future possibilities ("You Ain't Gonna Need It" - YAGNI).
**Best Practice**: Focus on clarity and the removal of duplication.
**Scrum Integration**: Keep designs lean during Sprint Planning to allow for agility as requirements evolve.
