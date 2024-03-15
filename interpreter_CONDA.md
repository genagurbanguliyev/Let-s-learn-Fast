### Conda
 conda create:
```sh
# if dir spesific
conda create --prefix ./venv python==3.10

# with name
conda create --name venv python==3.10
```

 activate-deactivate:
```sh
conda activate ./venv # or name of venv
conda deactivate
```

conda install packages:
```sh
conda install fastapi
# conda install --conda-forge fastapi

# install from requirements.txt file
conda install -file requirements.txt
```
 
 conda list of venvs:
```sh
conda env list
```

conda list of installed packages(after activate venv):
```sh
conda list
```

conda clean cache
```sh
pip cache purge

# show cashes:
pip cashe list
```

- `conda list` _gives you list of packages used for the environment_
    
- `conda list -e > requirements.txt` _save all the info about packages to your folder_
    
- `conda env export > <env_name>.yml`

