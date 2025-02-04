# 11. Python modules

## 11.1. Modules and Imports

Python modules help organize code into reusable components, making programs more maintainable and scalable. Understanding how to work with modules is essential for building professional Python applications.

### 11.1.1. Import statements 

The import statement allows you to use code from other Python files. There are several ways to import:

```
# Basic import
import math

# Import specific items
from math import sqrt

# Import with alias
import pandas as pd

# Import multiple items
from math import sqrt, pi

# Import all (generally not recommended)
from math import *
```

### 11.1.2. Creating modules

A module is simply a Python file containing functions, classes, and variables. Here's how to create and use them:

**Method**
1. In your Jupyter notebook, type `%pwd` and this will give you the current working directory of Jupyter

2. In the current working directory, use Notepad++ to save the code below and rename it <your name>.py. Make sure that you save it as a Python file 

```
# <your name>.py
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def random_function(a, b, c):
    return a*-6 + b*5 - c*10
```

3. In Jupyter, try with the following:
```
import <your name>

result1 = <your name>.add(5, 3)
result2 = <your name>.subtract(5, 3)
result3 = <your name>.random_function(5, 3, 4)

print(result1)
print(result2)
print(result3)
```

## 11.2. Package management and virtual environments

### 11.2.1. Using pip

Pip is Python's package installer. It helps you install and manage third-party packages.

```
# Basic installation
pip install pandas

# Install specific version
pip install pandas==1.4.2

# List installed packages
pip list
```

### 11.2.2. Virtual environments

Virtual environments create isolated Python environments for different projects, preventing package conflicts.

```
# Create virtual environment
python -m venv myenv

# Activate virtual environment
# On Windows:
myenv\Scripts\activate

# On Unix/MacOS:
source myenv/bin/activate

# Deactivate
deactivate
```
