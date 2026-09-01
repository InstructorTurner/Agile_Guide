# 🐧 WSL Guide (Windows Subsystem for Linux)

## 🚀 Getting Started
### Installation
1.  Open PowerShell as Admin: `wsl --install`
2.  Restart computer.
3.  Set up your username and password when prompted.

### Common Commands
| Action | Command | Description |
| :--- | :--- | :--- |
| **List Distros** | `wsl -l -v` | See installed distros and versions |
| **Shutdown** | `wsl --shutdown` | Kill all running WSL instances |
| **Update** | `wsl --update` | Update WSL kernel |
| **Set Default** | `wsl -s <distro>` | Change default Linux distro |

## 📂 File System Tips
*   **Linux $\rightarrow$ Windows:** `/mnt/c/Users/YourUser/`
*   **Windows $\rightarrow$ Linux:** Type `\\wsl$` in File Explorer.
*   **⚠️ Performance Rule:** Always keep your project files inside the Linux file system (e.g., `/home/username/projects/`) rather than `/mnt/c/`. Git and NPM are significantly faster this way.

## 🛠️ Integration with VS Code
1.  Install the **WSL extension** in VS Code.
2.  In your WSL terminal, navigate to your project and type: `code .`
3.  VS Code will launch in "Remote" mode, running the server on Linux while the UI is on Windows.
