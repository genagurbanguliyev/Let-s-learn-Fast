---
Technology: system_ubuntu
tags:
  - bash
  - "#port"
  - "#disable"
created_at: 2024-09-26
---
### show if used then disable given port:

##### Example Steps:

1. **Identify the Process Using the Port**:
    `sudo lsof -i :8000`
    
    This command lists the process using port 8000. Suppose the output shows that the process with PID `12345` is using the port.
    
2. **Terminate the Process**:
    
    `sudo kill -9 12345`
    
    This forcefully terminates the process with PID `12345`.
    
3. **Verify the Port is Free**:
    
    `sudo lsof -i :8000`
    
    If the port is free, this command should not return any output.