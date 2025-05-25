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

## 📌 More Git Commands (Coming Soon)
- `git status`
- `git commit -m "message"`
- `git push`
- `git pull`
- `git log`
- `git reset`
- `git stash`

---

_Keep this note updated as you progress. Clean commits = clean codebase._
