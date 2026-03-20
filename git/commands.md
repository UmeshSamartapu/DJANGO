```bash
git add .
git commit -m " * "
git push -u origin main
```

---

# 🧠  Absolute Basics

👉 Goal: Understand what Git is and start using it locally

### 🔹 Setup & Identity

```bash
git --version
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

### 🔹 Initialize Repo

```bash
git init
```

### 🔹 Basic Workflow

```bash
git status
git add file.txt
git add .
git commit -m "first commit"
```

### 🔹 View History

```bash
git log
```

---

# 🌱 1️⃣ BEGINNER LEVEL

👉 Goal: Work with files, undo mistakes, basic branching

### 🔹 File Operations

```bash
git rm file.txt
git mv old.txt new.txt
```

### 🔹 Undo Changes

```bash
git restore file.txt
git restore --staged file.txt
git reset HEAD file.txt
```

### 🔹 Commit Editing

```bash
git commit --amend
```

### 🔹 Branch Basics

```bash
git branch
git branch new-branch
git checkout new-branch
# OR modern:
git switch new-branch
```

---

# 🌿 2️⃣ INTERMEDIATE LEVEL

👉 Goal: Work with GitHub + collaboration

### 🔹 Connect to GitHub

```bash
git remote add origin https://github.com/username/repo.git
git remote -v
```

### 🔹 Push & Pull

```bash
git push -u origin main
git push
git pull
```

### 🔹 Clone Repo

```bash
git clone https://github.com/username/repo.git
```

### 🔹 Branching + Merging

```bash
git checkout -b feature-branch
git merge feature-branch
```

### 🔹 Fetch Updates

```bash
git fetch
```

---

# 🚀 3️⃣ ADVANCED LEVEL

👉 Goal: Professional workflows, debugging, clean history

### 🔹 Rebase (clean history)

```bash
git rebase main
git rebase -i HEAD~3
```

### 🔹 Stashing

```bash
git stash
git stash pop
git stash list
```

### 🔹 Reset (⚠️ powerful)

```bash
git reset --soft HEAD~1
git reset --mixed HEAD~1
git reset --hard HEAD~1
```

### 🔹 Cherry Pick

```bash
git cherry-pick <commit-id>
```

### 🔹 Tagging (releases)

```bash
git tag v1.0
git push origin v1.0
```

### 🔹 Logs & Debugging

```bash
git diff
git blame file.txt
git show <commit-id>
```

---

# 🧑‍💻 4️⃣ PRO / REAL-WORLD (Bonus)

👉 Used in teams, DevOps, CI/CD

### 🔹 GitHub Workflow (PR-based)

```bash
git checkout -b feature/login
git push origin feature/login
```

➡ Then create Pull Request on GitHub

### 🔹 Sync Fork

```bash
git remote add upstream https://github.com/original/repo.git
git fetch upstream
git merge upstream/main
```

### 🔹 Clean Repo

```bash
git clean -fd
```

### 🔹 Submodules

```bash
git submodule add <repo-url>
git submodule update --init
```

---

# 📊 QUICK SUMMARY TABLE

| Level        | Focus                  | Key Commands                  |
| ------------ | ---------------------- | ----------------------------- |
| Scratch      | Setup + basic commits  | `init`, `add`, `commit`       |
| Beginner     | File control + undo    | `restore`, `branch`, `switch` |
| Intermediate | GitHub + collaboration | `push`, `pull`, `clone`       |
| Advanced     | History + debugging    | `rebase`, `stash`, `reset`    |
| Pro          | Team workflows         | PR, fork sync, submodules     |

---

# 💡 PRO TIP (for YOU 🚀)

Since you're working on:

* Django
* ML models
* FastAPI
* MERN projects

👉 You should **master this workflow first:**

```bash
git init
git add .
git commit -m "initial"
git branch -M main
git remote add origin <repo>
git push -u origin main
```

---
