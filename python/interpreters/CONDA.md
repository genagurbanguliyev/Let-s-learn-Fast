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
conda activate ./venv # or name of venv or path/to/env
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

conda clean cache
```sh

```

onda list of installed packages(after activate venv):
```sh
conda list # _gives you list of packages used for the environment

#_save all the info about packages to your folder_
conda list -e > requirements.txt
# or 
conda env export > <env_name>.yml
```

#### conda env list problem
conda environments list comes from here: `~/.conda/environments.txt` You can add your env path here. WORKS 100%

> _**in UBUNTU you can open terminal and type: `nano ~/.conda/environments.txt`**_

activate env: `conda avtivate <path/to/env>` or if you inside project folder on terminal, you can run: `conda activate ./venv`

***
conda env remove:
```sh
#remove if create env with prefix
conda env remove --prefix=path/to/env/

# remove with name
conda env remove --name myenv
```

conda envs_dirs:
```sh
# show all dirs
conda config --show envs_dirs

# remove envs_dirs:
conda config --remove envs_dirs /path/to/envs_dirs
```