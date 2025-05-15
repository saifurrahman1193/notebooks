

# 🔄 Git Rebase Guide

When you use Git to rebase, each commit is applied to your branch.  
When merge conflicts occur, you are prompted to address them.

For more advanced options for your commits, use an **interactive rebase**.

---

## ✅ Prerequisites

- You must have permissions to **force push** to branches.

---

## ▶️ Rebase Your Branch Against the Target Branch

### Step 1: Open a terminal and change to your project directory

---

### Step 2: Fetch the latest contents of the target branch  
(Example: target branch is `main`)

```bash
git fetch origin main
```

---

### Step 3: Check out your working branch

```bash
git checkout my-branch
```

---

### Step 4 (Optional): Create a backup of your branch

```bash
git branch my-branch-backup
```

> ⚠️ Changes added to `my-branch` after this point are lost if you restore from the backup.

---

### Step 5: Rebase your branch onto `main`

```bash
git rebase origin/main
```

---

### Step 6: If merge conflicts occur

- Resolve the conflicts in your editor.

#### Stage the resolved changes:

```bash
git add .
```

#### Continue the rebase:

```bash
git rebase --continue
```

---

### Step 7: Force push your changes safely

```bash
git push origin my-branch --force-with-lease
```

> ✅ `--force-with-lease` is safer than `--force` because it ensures you don’t overwrite others’ work.

---



# Abort 

```
git rebase --abort
```




# Doc
- https://git-scm.com/docs/git-rebase
- https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase





```
git fetch origin main
git rebase origin/main
git rebase --continue
git add .

git rebase --continue
git add .

git rebase --continue
git add .

git rebase --skip
```