Python Package
====
# Getting Started
## Building from Source
### Installing Spark

> **Note:** The default configuration is for Hadoop 2.7.3. If building against
> a different version of Hadoop, please pass `-Dhadoop.version=<HADOOP_VERSION>`
> to the Maven command.

This approach entails three main bottlenecks: 

  1. __scaling the workflow__ comes down to scaling each of the individual
     tools,
  2. the __stability of the workflow__ heavily depends on the consistency of
     intermediate file formats, and
  3. __writing to and reading from disk__ is a major slow-down.

## Instructions to execute a Python package having two funcitons
1. Create a folder named 'package'
2. Create an empty file titled '__int__.py' (this will tell the interpreter that its a Python package)
3. Create a file named 'fn1.py' with a function in it.
4. Create a file named 'fn2.py' with another function in it.
5. Create a file named 'test.py' with a set of instructions to execute fn1 and fn2 functions
6. Open Terminal and Log into the folder 'Package'
7. Type in the follwoing command to execute the test.py file:
```bash
$ git clone https://github.com/rajputakhil/package.git
$ cd package
$ chmod a+x test.py
```
8. Type "python test.py" to execute the Python code

```python
def sasas()
  asasas
```

1. Create a folder named 'Package'

2. Create an empty file titled '__int__.py' (this will tell the interpreter that its a package)

3. Create a file named 'fn1.py' with a function in it.

'''python
def functionOne():
    print("This is Function One")
    return
'''

4. Create a file named 'fn2.py' with another function in it.

'''python
def functionTwo():
    print("This is Function Two")
    return
'''

5. Create a file named 'test.py' with a set of instructions to execute fn1 and fn2 functions.

'''python
import fn1, fn2
fn1.functionOne()
fn2.functionTwo()
'''

6. Open Terminal and Log into the folder 'Package'

7. Type in the follwoing command to execute the test.py file:

chmod a+x test.py

8. Type "python test.py" to execute the Python code
