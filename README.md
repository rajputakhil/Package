# package
Instructions to execute a Python package having two funcitons

1. Create a folder named 'Package'

2. Create an empty file titled '__int__.py' (this will tell the interpreter that its a package)

3. Create a file named 'fn1.py' with a function in it.

# def functionOne():
#   print("This is Function One")
#   return

4. Create a file named 'fn2.py' with another function in it.

# def functionTwo():
#   print("This is Function Two")
#   return

5. Create a file named 'test.py' with a set of instructions to execute fn1 and fn2 functions.

'''
import fn1, fn2
fn1.functionOne()
fn2.functionTwo()
'''

6. Open Terminal and Log into the folder 'Package'

7. Type in the follwoing command to execute the test.py file:

chmod a+x test.py

8. Type "python test.py" to execute the Python code
