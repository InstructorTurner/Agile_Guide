# 💻 VS Code Setup Guide

## 🧩 Recommended Extensions
| Extension | Purpose |
| :--- | :--- |
| **ESLint** | Catch JS/TS errors early |
| **Prettier** | Auto-format code on save |
| **Docker** | Manage containers/images from IDE |
| **PostgreSQL** | Run queries without leaving VS Code |
| **GitLens** | Advanced git history and blame |
| **WSL** | Essential for working in WSL2 environments |
| **Prisma / Adonis** | Language support for backend frameworks |

## ⚙️ Recommended Settings (`settings.json`)
```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit"
  },
  "files.autoSave": "onFocusChange",
  "terminal.integrated.defaultProfile.windows": "Ubuntu-22.04"
}
```

## ⌨️ Essential Shortcuts
| Shortcut | Action |
| :--- | :--- |
| `Ctrl + P` | Quick Open File |
| `Ctrl + Shift + P` | Command Palette |
| `Ctrl + \` | Split Editor |
| `Ctrl + \`` | Toggle Integrated Terminal |
| `Alt + Shift + F` | Format Document |
