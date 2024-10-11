---
Technology: Git
tags:
  - "#git_branch"
  - "#git_merge"
created_at: 2024-08-23
---
### Work with git branch

**To list all existed branches:**
```
git branch
```

**To create a new Git branch:**
<small>This command will create a new branch pointing to the same commit as your current branch. </small>
```
git branch <new_branch_name>
```

**switch to the new(other) branch:**
```
git checkout <branch_name>
```

**To merge two Git branches:**
- 1. Make sure you're on the branch you want to merge into:
```
git checkout main  # Assuming you want to merge into the main branch
```

- 2. Merge the other branch:
```
git merge <feature_branch>
```
<small>This command will merge the changes from the `feature_branch` into the current branch (`main` in this example).</small>

- 2. Merge the other branch:
```
git merge <feature_branch>
```
<small>This command will merge the changes from the `feature_branch` into the current branch (`main` in this example).</small>

***
**Push the "main" branch to "main_origin":**
```
git push main_origin main
```