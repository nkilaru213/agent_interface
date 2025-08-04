# 🌐 Opening Repositories in VS Code Web IDE via Coder UI

This guide explains how to open your cloned Git repository in **VS Code Web IDE** using the **Coder platform**.

---

## 🚀 Prerequisites

- A workspace created in **Coder** with the VS Code Web IDE template
- Git installed in the workspace container
- Repository already cloned using Git + Personal Access Token (PAT)

---

## 🧭 Steps to Open Your Project in VS Code Web (via Coder)

### 1. **Login to Coder**
- Go to your Coder workspace portal (e.g., `https://your-coder-instance.com`)
- Authenticate using SSO or credentials

### 2. **Start Your Workspace**
- From your Coder dashboard, locate your workspace and click **"Start"**
- Wait for the workspace to fully initialize

### 3. **Launch VS Code Web IDE**
- Once running, click the **"Open in VS Code Web"** button or the **VS Code icon** from the workspace UI

### 4. **Open the Project Folder**
- Use the VS Code File Explorer to open the cloned repository directory:
  - Click **File > Open Folder**
  - Navigate to your Git project folder (e.g., `/home/coder/your-repo`)
  - Click **Open**

> Your code is now ready to be viewed, edited, committed, and pushed—all within the browser.

---

## 💾 Git User Configuration (if not already set)

```bash
git config --global user.name "Your Full Name"
git config --global user.email "your.email@example.com"
```

---

## 🔄 Making Git Changes in VS Code Web

1. Modify files using the editor
2. Use the Source Control panel on the left sidebar:
   - Stage changes
   - Write commit messages
   - Push or pull changes

> First push may prompt authentication. Use your **GitHub username** and **Personal Access Token** as the password.

---

## 📌 Notes

- Workspace folders persist across sessions unless explicitly deleted.
- Ensure your token scopes allow `repo` access.
- Credential storage depends on the Coder workspace config (some setups support Git credential helpers).

---

## 📚 References

- [Coder Docs](https://coder.com/docs)
- [GitHub Personal Access Tokens](https://github.com/settings/tokens)
- [VS Code in the Browser](https://vscode.dev)
