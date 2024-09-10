**1. Create the tag:**
```
git tag <tag_name>
```

**2. Push the tag to the remote repository:**
```
git push origin <tag_name>
```

***

**Additional notes:**

- You can create annotated tags by adding a message using the `-a` option: `git tag -a v1.0 -m "Version 1.0"`.
- To list all existing tags, use the `git tag` command.
- To delete a tag, use the `git tag -d <tag_name>` command.
- If you want to push all tags to the remote repository, use the `git push --tags` command.