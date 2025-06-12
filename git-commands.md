# 📘 Git Command Reference – Detailed Guide with Examples and Interview Questions

---

## 1. `git add`

### ✅ Description
Stages changes (new, modified, deleted files) to be committed.

### 🖊️ Syntax
```bash
git add <file-name>     # Add a specific file
git add .               # Add all changes in the current directory
git add -A              # Add all changes (including deletions)
````

### 🧪 Example

```bash
git add index.html
git add .
```

### 💡 Use Case

Prepare your working changes for committing.

### ❓ Interview Questions

* What’s the difference between `git add .` and `git add -A`?
* Can you add a deleted file using `git add`?

---

## 2. `git commit`

### ✅ Description

Records changes to the local repository.

### 🖊️ Syntax

```bash
git commit -m "Your commit message"
git commit -a -m "Commit with auto add for tracked files"
```

### 🧪 Example

```bash
git commit -m "Fix header layout bug"
```

### 💡 Use Case

Log a snapshot of your project’s state at a particular time.

### ❓ Interview Questions

* What’s the role of the commit message?
* Can you commit without staging?

---

## 3. `git push`

### ✅ Description

Uploads local repository content to a remote repo.

### 🖊️ Syntax

```bash
git push origin main     # Pushes to the main branch
```

### 🧪 Example

```bash
git push origin feature/login
```

### 💡 Use Case

Collaborating with others by sharing changes to GitHub, GitLab, etc.

### ❓ Interview Questions

* What’s the difference between `git push` and `git fetch`?
* What happens if someone else pushed changes before you?

---

## 4. `git revert`

### ✅ Description

Creates a new commit that undoes a previous commit, preserving history.

### 🖊️ Syntax

```bash
git revert <commit-hash>
```

### 🧪 Example

```bash
git revert a1b2c3d4
```

### 💡 Use Case

Undo a commit safely on a shared branch.

### ❓ Interview Questions

* What’s the difference between `git revert` and `git reset`?
* When would you use revert on a production branch?

---

## 5. `git reset`

### ✅ Description

Undoes commits and/or staged changes. Can be soft, mixed, or hard.

### 🖊️ Syntax

```bash
git reset --soft <commit-hash>
git reset --mixed <commit-hash>
git reset --hard <commit-hash>
```

### 🧪 Example

```bash
git reset --hard HEAD~1
```

### 💡 Use Case

Rollback to a known good state during development.

### ❓ Interview Questions

* Explain `--soft`, `--mixed`, and `--hard`.
* Is `git reset` safe on a public branch?

---

## 6. `.gitignore`

### ✅ Description

Specifies intentionally untracked files to ignore.

### 🖊️ Syntax (in `.gitignore`)

```
node_modules/
*.log
.env
```

### 🧪 Example

Place this in your `.gitignore`:

```
dist/
*.tmp
```

### 💡 Use Case

Prevent sensitive or unnecessary files from being tracked.

### ❓ Interview Questions

* How does `.gitignore` work with already tracked files?
* Can you ignore a file in a subfolder only?

---

## 7. `git clean`

### ✅ Description

Removes untracked files and directories.

### 🖊️ Syntax

```bash
git clean -f
git clean -fd
git clean -n
```

### 🧪 Example

```bash
git clean -fd
```

### 💡 Use Case

Clean working directory during builds or before commits.

### ❓ Interview Questions

* What’s the difference between `git clean` and `git reset`?
* What happens if you run `git clean -fdx`?

---

## 8. `git status`

### ✅ Description

Shows the current state of the working directory and staging area.

### 🖊️ Syntax

```bash
git status
```

### 🧪 Example

```bash
git status
```

### 💡 Use Case

Check which files are staged, unstaged, or untracked.

### ❓ Interview Questions

* How does `git status` help in debugging?
* Can you use `git status` to view remote changes?

---

## 9. `git flow`

### ✅ Description

A branching model for Git developed by Vincent Driessen. Uses feature, release, and hotfix branches.

### 🖊️ Syntax

```bash
git flow init
git flow feature start <name>
git flow feature finish <name>
```

### 🧪 Example

```bash
git flow release start v1.0
```

### 💡 Use Case

Managing large-scale software development projects with multiple releases.

### ❓ Interview Questions

* What are the advantages of `git flow`?
* When should you avoid `git flow`?

---

## 10. `git log`

### ✅ Description

Shows the commit history.

### 🖊️ Syntax

```bash
git log
git log --oneline
git log --graph --all
```

### 🧪 Example

```bash
git log --oneline --graph
```

### 💡 Use Case

Review project history, debug issues, or find changes.

### ❓ Interview Questions

* How can you filter `git log` by author or date?
* What’s the difference between `git log` and `git reflog`?

---

## 📌 Summary Table

| Command      | Purpose                     | Risk Level   |
| ------------ | --------------------------- | ------------ |
| `git add`    | Stage changes               | Low          |
| `git commit` | Save changes to local repo  | Low          |
| `git push`   | Upload to remote            | Medium       |
| `git revert` | Undo via a new commit       | Safe         |
| `git reset`  | Undo commits or staging     | Risky (hard) |
| `.gitignore` | Exclude files from tracking | Safe         |
| `git clean`  | Remove untracked files      | Risky        |
| `git status` | See current changes         | Safe         |
| `git flow`   | Workflow management         | Safe         |
| `git log`    | Show commit history         | Safe         |

```


