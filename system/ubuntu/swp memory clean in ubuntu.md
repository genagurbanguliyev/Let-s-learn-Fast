---
Technology: system_ubuntu
tags:
  - "#swp"
  - cache
created_at: 2024-10-02
---
### how to swp memory clean in ubuntu?
Here's how to clean swap memory in Ubuntu:### Step-by-step process:

1. Check current swap usage
2. Disable swap
3. Enable swap again
4. Verify changes

### Key points to consider:
- This process will move data from swap back to RAM
- Ensure you have enough free RAM before proceeding
- Be cautious when running these commands, especially on systems with limited resources

### Implementation:
1. First, check your current swap usage:
```bash
free -h
```

2. To clear swap memory, run the following command:
```bash
sudo swapoff -a && sudo swapon -a
```

This command disables all swap spaces (`swapoff -a`) and then re-enables them (`swapon -a`). This effectively clears the swap memory [1](https://askubuntu.com/questions/1357/how-to-empty-swap-if-there-is-free-ram).

3. After running the command, verify the changes:

```bash
free -h
```