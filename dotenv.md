# Using .env files
Do not store credentials in code.
It is safer to store credentials in a file named '*.env' and format it like so:

```
USERNAME=my_username
PASSSWORD=my_password
```

```python
from dotenv import load_dotenv, dotenv_values  # requires pip install python-dotenv

load_dotenv()
USERNAME = dotenv_values()["USERNAME"]
PASSWORD = dotenv_values()["PASSWORD"]
```
