# 🔐 Git Setup with GitHub Personal Access Token (PAT)

This guide walks you through the steps to configure Git on a new machine and authenticate using a **GitHub Personal Access Token (PAT)**.

---

## 📌 Prerequisites

- A GitHub account: https://github.com
- Git installed (`git --version` to check)
- PAT generated via GitHub settings

---

## 🔧 Step 1: Generate a Personal Access Token (PAT)

1. Go to: [https://github.com/settings/tokens](https://github.com/settings/tokens)
2. Click **"Generate new token"** → choose **"Tokens (classic)"**
3. Fill in:
   - **Note**: e.g., `Work Laptop Git Access`
   - **Expiration**: e.g., 90 days
   - **Scopes**: select at least `repo`
4. Click **Generate token**
5. **Copy and store the token securely** — this will be your Git password

---

## 👤 Step 2: Configure Git User Identity

```bash
git config --global user.name "Your Full Name"
git config --global user.email "your.email@example.com"
```

> Omit `--global` if you want to configure per repository.

---

## 🔑 Step 3: Use the Personal Access Token

When cloning a private repo or pushing changes, use:

### Example:
```bash
git clone https://github.com/your-username/your-repo.git
```

When prompted:

- **Username**: your GitHub username  
- **Password**: paste your **Personal Access Token**

---

## 💾 Step 4: Save Credentials (Optional)

To avoid entering the PAT every time, configure Git’s credential helper.

### macOS:
```bash
git config --global credential.helper osxkeychain
```

### Windows:
```bash
git config --global credential.helper manager-core
```

### Linux (⚠️ stores in plain text):
```bash
git config --global credential.helper store
```

---

## 🔄 Step 5: Test Git Workflow

### Clone a repo:
```bash
git clone https://github.com/your-username/your-repo.git
```

### Make changes and push:
```bash
cd your-repo
touch test.txt
git add test.txt
git commit -m "Initial commit"
git push origin main
```

If this is your first push, Git will prompt for credentials and store them based on your credential helper.

---

## 🚨 Tips

- Never commit your token to any repository.
- Revoke tokens if exposed: [https://github.com/settings/tokens](https://github.com/settings/tokens)
- Rotate your PATs regularly for security.

---

## 📚 References

- GitHub Docs: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token
- Git Docs: https://git-scm.com/doc
