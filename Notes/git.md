# Git Notes

## 🔹 `git add` Variants Explained

### `git add .` — Add from Current Directory Down
Adds:
- ✅ Modified files  
- ✅ New/untracked files  

Ignores:
- ❌ Deletions  

**Scope:**  
Only in the current directory and its subdirectories

---

### `git add -u` — Update Tracked Files Only
Adds:
- ✅ Modified files  
- ✅ Deleted files  

Ignores:
- ❌ New/untracked files  

**Scope:**  
Entire repo (or restricted to path if you provide one)

---

### `git add -A` — Stage Absolutely Everything
Adds:
- ✅ Modified files  
- ✅ New/untracked files  
- ✅ Deleted files  

**Scope:**  
Entire working directory (regardless of current path)

---

### ✅ When to Use Each

| Command       | Use Case                                                              |
|---------------|-----------------------------------------------------------------------|
| `git add .`   | You only want to stage new + modified files in the current folder     |
| `git add -u`  | You want to stage changes and deletions, but not new untracked files  |
| `git add -A`  | You want to stage everything — full sync with working directory       |

---

## 🔹 `git status` — Check Current State

Shows:
- ✅ Files staged for commit
- ✅ Files modified but not staged
- ✅ Untracked files

**Use Case:**
- Before committing, use this to verify what will be included

**Tip:** Run this often to stay aware of your repo’s status

---

## 🔹 `git commit -m "message"` — Save a Snapshot

Commits:
- ✅ All staged changes with a message

**Best Practices:**
- Use clear, concise commit messages (e.g., `"Add login feature"`)

**Note:** Only staged files are included. Run `git add` before committing.

---

## 🔹 `git push` — Upload Local Commits to Remote

Sends:
- ✅ Your local commits to GitHub (or any remote origin)

**Use Case:**
- Share your changes with team or back up your work

**Example:**
```bash
git push origin main
```

---

## 🔹 `git pull` — Sync with Remote

Does:
- ✅ Fetch latest changes from remote
- ✅ Merge them into your local branch

**Use Case:**
- Always pull before you start new work to avoid conflicts

**Example:**
```bash
git pull origin main
```

---

## 🔹 `git log` — View Commit History

Shows:
- ✅ List of past commits with hash, author, and message

**Flags:**
- `--oneline`: Brief format
- `--graph`: Visual branch tree

**Example:**
```bash
git log --oneline --graph
```

---

## 🔹 `git reset` — Undo Changes (Advanced)

Types:
- `--soft`: Uncommit but keep changes staged
- `--mixed` (default): Uncommit + unstage changes
- `--hard`: DANGEROUS — Discard everything

**Example:**
```bash
git reset --soft HEAD~1  # Undo last commit, keep changes staged
```

**Use With Caution:**
- Always double-check before using `--hard`

---

## 🔹 `git stash` — Save Changes for Later

Use Case:
- ✅ Temporarily save uncommitted changes without committing

**Basic Commands:**
```bash
git stash           # Stash current changes
git stash list      # View stashes
git stash pop       # Reapply and remove latest stash
git stash apply     # Reapply without removing from stash
```

**Great For:**
- Switching branches quickly without losing progress

---

## 🧠 Pro Tip:
Use a consistent workflow:
```bash
git status
# -> Review changes
git add .
# -> Stage changes
git commit -m "Your message"
# -> Commit snapshot
git push
# -> Send to remote
```

---
