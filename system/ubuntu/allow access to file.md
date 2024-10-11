---
Technology: system_ubuntu
tags:
  - bash
  - "#permission"
created_at: 2024-09-26
---
### Working with permissions
```bash
sudo chmod a+rwx <file_path>
```
<small>This command will add read, write, and execute permissions for all users (owner, group, and others) to the specified file.</small>

Here's a breakdown of the permissions:

- `a`: All users (owner, group, and others)
- `+`: Add permissions
- `r`: Read permission
- `w`: Write permission
- `x`: Execute permission

By using this command, you will ensure that all users have full access to the file.