# 10 SDD Case Study: The Photo Organizer

[← Back to Index](index.md)

To see SDD in action, let's track a feature from a raw idea to a converged implementation.

## Phase 1: Human-First Breakdown (The Brain)
**The Idea**: A simple app to organize photos into albums.

**Hand-written notes**:
- Need a main page with a grid of albums.
- Albums should be grouped by the date they were created.
- User should be able to drag an album to reorder it.
- No nested albums (keep it simple!).
- Inside an album: a tile view of photos.
- *Constraint*: No cloud storage. Everything is local.

## Phase 2: Conversational Refinement (The Dialogue)
**Developer -> OpenCode**: "I have this breakdown for a photo app. What am I missing?"
**OpenCode**: "You mentioned dragging to reorder, but should that order be saved permanently? Also, how do you handle photos that don't have a date metadata?"
**Developer**: "Yes, save the order. If no date, put them in an 'Unsorted' album at the bottom."

## Phase 3: Speckit Implementation (The Tooling)

1. **Constitution**: `/speckit.constitution "Prioritize local-first storage and accessible UI."`
2. **Specify**: `/speckit.specify "Build a photo album organizer. Albums are grouped by date, re-orderable via drag-and-drop, and contain tile-based photo previews. No nesting. Use an 'Unsorted' album for photos without dates."`
3. **Plan**: `/speckit.plan "Use Vite, vanilla JS, and SQLite for local metadata storage."`
4. **Tasks**: `/speckit.tasks` -> Agent generates 12 tasks (DB schema -> File AOpenCode -> UI Grid -> Drag-and-Drop logic).
5. **Implement**: `/speckit.implement` -> Agent writes the code.
6. **Converge**: `/speckit.converge` -> Agent notices the 'Unsorted' album logic was missed. It adds a new task.
7. **Final Loop**: Implement -> Converge -> **Converged**.

## Result
The developer didn't just "prompt" an app into existence. They architected the logic, refined the edge cases through dialogue, and used a structured process to ensure the implementation perfectly matched the intent.
