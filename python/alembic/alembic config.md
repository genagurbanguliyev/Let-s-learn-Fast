#migration
for use alembic for migrations:
1. install `alembic`

2. Run init command in root directory:
```shell
alembic init alembic # last alembic is folder name
```

After this command create `alembic.ini` file and `alembic_name` folder inside the folder has `env.py` file and there some configurations:

```python
...
from sqlmodel import SQLModel

# just import all models
from app.model import *  # noqa  
  
  
from app.core.config import configs  
  
# this is the Alembic Config object, which provides  
# access to the values within the .ini file in use.  
config = context.config  
  
# Interpret the config file for Python logging.  
# This line sets up loggers basically.  
if config.config_file_name is not None:  
    fileConfig(config.config_file_name)  
  
# ======================== My configs ========================  
config.set_main_option("sqlalchemy.url", configs.DATABASE_URL)  
target_metadata = SQLModel.metadata  
  
  
def run_migrations_offline() -> None:
...
```

After these configurations you can do migrations as showed here: [[migration]]

