### PIP
 python venv:
```sh
# if dir spesific
python -m venv myvenv
# python3.9 -m venv myvenv
```

 activate-deactivate:
```sh
# Windows
.\myvenv\Scripts\Activate.ps1

# Linux
source myvenv/bin/activate

```

 pip install packages:
```sh
pip install fastapi

# install from requirements.txt file
pip install -r requirements.txt
```


pip list of installed packages(after activate venv):
```sh
# show in terminal:
pip freeze

# get reqirements.txt file
pip freeze > requirements.txt
```

pip clean cache

With pip 20.1 or later, you can do:

- `pip cache remove matplotlib`: removes all wheel files related to matplotlib from pip's cache.
- `pip cache purge`: to clear all wheel files from pip's cache.
- `pip cache dir`: to get the location of the cache.

If you want to not use the pip cache for some reason (which is a bad idea, according [the official docs](https://pip.pypa.io/en/stable/topics/caching/#disabling-caching)), your options are:

- `pip install --no-cache-dir <package>`: install a package without using the cache, for just this run.
- `pip config set global.no-cache-dir false`: configure pip to not use the cache "globally" (in all commands).