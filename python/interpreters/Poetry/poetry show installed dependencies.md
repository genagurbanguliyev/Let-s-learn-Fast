`poetry show`

This command will display a list of all installed dependencies, including their names and versions.

If you're interested in checking for outdated dependencies—those that have newer versions available—you can use the `--outdated` flag with the `poetry show` command:

`poetry show --outdated`

This command will list all dependencies that have updates available, showing the current version installed and the latest version available [5](https://www.geeksforgeeks.org/managing-dependencies-with-python-poetry/).

Additionally, if you want to see the dependency tree, including transitive dependencies (dependencies of your dependencies), you can add the `-t` or `--tree` option:

`poetry show --tree`