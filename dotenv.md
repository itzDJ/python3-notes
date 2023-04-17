# Using .env files
Do not store credentials in code; store credentials in a file named '*.env' and format it like so:

```
USERNAME=my_username
PASSSWORD=my_password
```

```python
from dotenv import load_dotenv  # requires pip install python-dotenv
from os import getenv

load_dotenv()
USERNAME = getenv("USERNAME")
PASSWORD = getenv("PASSWORD")
```
