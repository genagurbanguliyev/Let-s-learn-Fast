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

conda clean cache
```sh
conda clean --all
```

conda update
```sh
conda update conda # udate only conda
conda update --all
```

