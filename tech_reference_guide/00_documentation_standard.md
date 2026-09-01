# 📏 Documentation Standards

To ensure this guide remains a high-quality resource, all contributions must follow these standards.

## ✍️ Content Guidelines
### 1. Be Concise
This is a **Cheat Sheet**, not a textbook. 
*   Use tables for commands.
*   Use short code blocks for examples.
*   Avoid long paragraphs; use bullet points.

### 2. Use a Consistent Structure
Every new guide page should follow this layout:
1.  **Title** (`# Tool Name`)
2.  **Quick Start/Common Commands** (Table format)
3.  **Code Examples** (Marked with language tags, e.g., \`\`\`javascript)
4.  **Gotchas/Tips** (Bullet points)

### 3. Adding New "Hurdles"
When you solve a technical problem that isn't in the guide:
1.  Identify which tool folder it belongs in.
2.  If it's a common pattern, add it to an existing file.
3.  If it's a unique problem, create a new file: `XX_problem_name.md`.
4.  Update the `README.md` Table of Contents.

## 🛠️ Formatting Rules
*   **File Naming:** Use numbered prefixes (e.g., `01_setup.md`) to maintain order.
*   **Links:** Use relative paths for internal links (e.g., `[Link](./folder/file.md)`).
*   **Images:** If adding screenshots, store them in an `/assets` folder and link relatively.

## ✅ Checklist Before PR
- [ ] Does this follow the "Concise" rule?
- [ ] Are code blocks tagged with the correct language?
- [ ] Is the README updated?
- [ ] Are relative links working?
