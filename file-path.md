When creating or accessing files, it's often helpful to use the absolute path to the intended location.
This allows the code to be run from anywhere.

```python
from pathlib import Path

# The absolute path of the python script being executed
current_script = Path(__file__).absolute()

# The absolute path of the parent directory of the python script being executed
file_dir = Path(__file__).absolute().parent
```
