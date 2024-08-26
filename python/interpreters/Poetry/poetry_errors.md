# Error not found in terminal:
if after installation poetry not found in terminal:
- **Check Installation Script Output:**
    
    When you ran the installation script, it should have indicated the directory where Poetry was installed. By default, this is `$HOME/.local/bin`.
    
- **Add Poetry to PATH:**
    
    Open your shell configuration file and add the Poetry binary path if it's not already present.    
    `nano ~/.bashrc`
    
    Add the following line to the end of the file:
    `export PATH="$HOME/.local/bin:$PATH"`
    
- **Reload the Shell Configuration:**
    
    After adding the above line, reload your shell configuration to update the PATH.
    `source ~/.bashrc`
    
- **Verify Poetry Installation:**
    
    Now, check the Poetry version to verify the installation.
    `poetry --version`