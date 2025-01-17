---
Technology: Git
tags:
  - reset_revert
created_at: 2024-10-04
---

There are two main ways to remove committed elements from your local **Git repository since you haven't pushed them yet**:

#### 1. Using `git reset` (Destructive):
This approach removes the commit entirely, including the changes it introduced. Be cautious, as this cannot be undone easily:
```bash
git reset HEAD~
```
**Explanation:**
 - This moves your HEAD pointer one commit back
- `git reset HEAD~`: The `~` after `HEAD` indicates going back one commit in the Git history. This detaches your HEAD from the most recent commit.

***

#### 2. Using `git revert` (Preferred):
This method creates a new commit that effectively undoes the changes introduced in the previous commit. It's generally preferred as it keeps a clear history of changes:
```
git revert HEAD
```
**Explanation:**
- `git revert HEAD`: This command analyzes the most recent commit (HEAD) and creates a new commit that reverses the changes introduced in that commit.

***

**Choosing the Best Method:**
- If you just want to completely discard the changes and the commit, use `git reset HEAD~`. However, be aware that this removes the commit from history.
- If you want to keep a record of the changes being undone and maintain a cleaner Git history, use `git revert HEAD`. This is the recommended approach in most cases.


***
**Choose the appropriate method based on your specific needs:**

- **`git revert`** is useful if you want to keep a record of the changes you're undoing.
- **`git reset --hard`** is a more drastic option that discards all changes since the last commit.
- **`git checkout`** is useful if you want to create a new branch to explore alternative versions of your code.