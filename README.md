Python Program = Modules + Packages
====

  1. This is a step-by-step demonstration to divide Python code base into clean, efficient __modules__ using Python __packages__.
  2. Additionally, you'll learn to __import__ and use your own packages, thus building your own Python program.

## Instructions to execute a Python package having two funcitons

1. Create a directory named __'package'__.

2. Create an empty file named ```__int__.py``` (this will tell the interpreter that its a package)

3. Create a file named 'fn1.py' with a function in it.

```python
def functionOne():
    print("This is Function One")
    return
```

4. Create another file named 'fn2.py' with a different function in it.

```python
def functionTwo():
    print("This is Function Two")
    return
```

5. Create a file named __'test.py'__ with a set of python code to execute __fn1__ and __fn2__ functions.

```python
import fn1, fn2
fn1.functionOne()
fn2.functionTwo()
```

6. Open Terminal and log into the folder __'package'__ and type in the follwoing command to execute __test.py__ file:

```bash
$ cd package
$ chmod a+x test.py
$ python3 test.py
```

7. The program __test.py'__ will get executed.

> **Note:** The program will run for both Python 2 as well as Python 3 version.
