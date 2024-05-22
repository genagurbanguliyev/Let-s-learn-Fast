#### Devlarative style:
```python
from sqlalchemy import String
from sqlalchemy.orm import DeclarativeBase, Mapped, mapped_column

class Base(DeclarativeBase):
	pass

class Users(Base):
	__tablename__ = "users"
	
	id: Mapped[int] = mapped_column(primary_key=True)
	username: Mapped[str] = mapped_column(String(30))
	password: Mapped[str]
```

#### Imperative style:
```python
from sqlalchemy import Metadata, Table, Column, String, Integer

metadata_obj = MetaData()

users_table = Table(
				'users',
				metada_obj,
				Column("id", Integer, primary_key=True),
				Column("username", String),
				Column("password", String)
)
```