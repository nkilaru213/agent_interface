# 🧑‍💻 Opening GitHub Repositories in VS Code Web IDE

After setting up Git and cloning a repository using a GitHub Personal Access Token (PAT), you can open the project in **Visual Studio Code Web IDE** to edit and manage your code without installing VS Code locally.

---

## 🌐 Option 1: Use `vscode.dev` (No Setup Required)

### 🔧 Steps:
1. Open your browser and go to:
   ```
   https://vscode.dev/github/your-username/your-repo
   ```
   > Replace `your-username` and `your-repo` with your actual GitHub repo URL.

2. Sign in with your GitHub account if prompted.
3. You can now browse, edit, and commit code using the browser-based VS Code experience.

---

## 🌐 Option 2: Open Local Clone in VS Code (Desktop or Web)

If you already cloned the repository using Git:

### 📁 Open in Local VS Code:
```bash
cd your-repo
code .
```

> This opens the current folder in **VS Code Desktop**. Requires `code` command-line tool (installed with VS Code).

### 💡 To Use in VS Code Web:
1. Open [https://vscode.dev](https://vscode.dev)
2. Press `Ctrl + O` or `Cmd + O` and select the folder.
3. (Optional) Use GitHub authentication in the sidebar for committing & pushing changes.

---

## 🧠 Notes:
- VS Code Web (`vscode.dev`) supports **lightweight development**, but lacks terminal access and some extensions.
- For full-featured development, use **GitHub Codespaces** or **VS Code Desktop**.
- You can also install the **GitHub Repositories** extension in VS Code for advanced GitHub integration.

---

## 🔐 Tip: Authenticate Git in Web IDE

If pushing changes fails in the Web IDE:
- Make sure you're signed into GitHub inside the editor (look for Accounts icon in bottom-left corner).
- PAT-based authentication may be required on first push.

---

## 📚 References
- [VS Code Web (vscode.dev)](https://vscode.dev)
- [GitHub Codespaces](https://github.com/features/codespaces)
- [VS Code GitHub Integration](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
