# AttributeError
### What is AttributeError?
Exception `AttributeError` raised when an attribute reference (see [Attribute references](https://docs.python.org/3/reference/expressions.html#attribute-references)) or assignment fails. (When an object does not support attribute references or attribute assignments at all, [`TypeError`](https://github.com/Sayad-Uddin-Tahsin/Solution-Hint/blob/main/Solutions.md#typeerror) is raised.)

The `name` and `obj` attributes can be set using keyword-only arguments to the constructor. When set they represent the name of the attribute that was attempted to be accessed and the object that was accessed for said attribute, respectively.

### When occoured?
It usually occoured when some invalid Attribute was called in code. Example:
```py
class Solution():
    def __init__(self):
        self.name = 'Solution of AttributeError'

print(Solution().name) # Solution of AttributeError
print(Solution().something) # raises AttributeError: 'Solution' object has no attribute 'something'
```
`print(Solution().something)` raised 
```py
AttributeError: 'Solution' object has no attribute 'something'
```
because there was no attribute set in the `Solution` class.

### How to Fix?
#### Handling
Errors and exceptions in Python can be handled using exception handling i.e. by using try and except in Python. With `try` & `except` the errors can be handled. Code:
```py
class Solution():
    def __init__(self):
        self.name = 'Solution of AttributeError'

try:
    print(Solution().name) # Solution of AttributeError
    print(Solution().something) # raises AttributeError: 'Solution' object has no attribute 'something'
except AttributeError:
    pass
```
Output:
```
Solution of AttributeError
```
The error didn't raised because you said to `pass` in `except`, by mentioning `AttributeError` after `except` you are telling the code to `pass` it when it's `AttributeError` only!

#### Solution: AttributeError
You can call the appropriate attribute to avoid this error, [Handling](https://github.com/Sayad-Uddin-Tahsin/Solution-Hint/blob/main/Solutions.md#handling) it is also a great way avoid crash!

# FileNotFoundError
### What is FileNotFoundError?
Raised when a file or directory is requested but doesn’t exist. Corresponds to errno [ENOENT](https://docs.python.org/3/library/errno.html#errno.ENOENT).

### Solution: FileNotFoundError
**Error**:
```py
FileNotFoundError: [Errno 2] No such file or directory
```

**Solution**:

This Type("FileNotFoundError") of error occurred when a File tried to opened in your code is not in this directory or the PATH is incorrect!
Recheck the file name or path, to solve this issue.


# IndexError
### What is IndexError?
Raised when a sequence subscript is out of range. (Slice indices are silently truncated to fall in the allowed range; if an index is not an integer, [`TypeError`](https://github.com/Sayad-Uddin-Tahsin/Solution-Hint/blob/main/Solutions.md#typeerror) is raised.)

This error occurs when an attempt is made to access an item in a list at an index which is out of bounds. The range of a list in Python is [0, n-1], where `n` is the number of elements in the list. When an attempt is made to access an item at an index outside this range, an `IndexError: list index out of range` error is thrown.

## 

### IndexError: list
**Error**:
```py
IndexError: list index out of range
```

**Solve**

There is no specific solve for this type of error. You've to get the range of the `list` and call that as the `index`. Index for a List is starts from 0. This image shows how the indexes are counted.

![image](https://user-images.githubusercontent.com/89304780/208110226-6d4c78d7-2b85-43d3-8817-fde00d5e26a3.png)

# KeyError
### What is KeyError?
Raised when a mapping (dictionary) key is not found in the set of existing keys. This is a Dictionary Example: 
```json
{"key": "value"}
```
This error occoured when the requested `key` is not in the dictionary.

### Solution: KeyError
**Error**:
```py
KeyError: 'key'
```

**Solve**

There is no specific solution for this error. You have to recheck the key and call with the right one. Note that, `key` is **CASE SENSITIVE**.

# ModuleNotFoundError
### What is ModuleNotFoundError?
A subclass of [ImportError](https://docs.python.org/3/library/exceptions.html#ImportError) which is raised by [import](https://docs.python.org/3/reference/simple_stmts.html#import) when a module could not be located. It is also raised when None is found in [sys.modules](https://docs.python.org/3/library/sys.html#sys.modules). It usually occoured when the Module used in code but not installed!

##

### ModuleNotFoundError: No module named
**Error**:
```py
No module named 'module_name'
```

**Solution**:
Install the Module in your PC. The Install syntax is `pip install <package>`. But in some case, `<package>` is not the same as the Module name. Get the Install Syntax by searching in [pypi.org](https://pypi.org/search/) or search `<module name> pypi` in Google you'll find a pypi page corresponding the Module's page in PyPi.


# NameError
### What is NameError?
Raised when a local or global name is not found. This applies only to unqualified names. The associated value is an error message that includes the name that could not be found.

The `name` attribute can be set using a keyword-only argument to the constructor. When set it represent the name of the variable that was attempted to be accessed.

##

### Why NameError occurred?
**1. Misspelled built-in functions:**

In the below example code, the print statement is misspelled hence NameError will be raised.
```py
name = input()
Print(name)
```

**2. Using undefined variables:**

When the below program is executed, NameError will be raised as the variable `name` is never defined because we've created `user` not `name`
```py
user = input()
print(name)
```

**3. Defining variable after usage:**

In the following example, even though the variable name is defined in the program, it is defined after its usage. Since Python interprets the code from top to bottom, this will raise NameError.
```py
print(name)
name = "Tahsin"
```

**4. Incorrect usage of scope:**

In the below example program, the variable geek is defined within the local scope of the assign function. Hence, it cannot be accessed globally. This raises NameError.
```py
def assign():
    geek = "GeeksforGeeks"
 
assign()
print(geek)
```

##

### Solution: NameError

Skipping the [above](https://github.com/Sayad-Uddin-Tahsin/Solution-Hint/blob/main/Solutions.md#why-nameerror-occurred) issues will solve the problem.


# TypeError
### What is TypeError?
Exception `TypeError` raised when an operation or function is applied to an object of inappropriate type. The associated value is a string giving details about the type mismatch.

This exception may be raised by user code to indicate that an attempted operation on an object is not supported, and is not meant to be. If an object is meant to support a given operation but has not yet provided an implementation, [NotImplementedError](https://docs.python.org/3/library/exceptions.html#NotImplementedError) is the proper exception to raise.

Passing arguments of the wrong type (e.g. passing a `list` when an `int` is expected) should result in a `TypeError`, but passing arguments with the wrong value (e.g. a number outside expected boundaries) should result in a [ValueError](https://docs.python.org/3/library/exceptions.html#ValueError).

##

### TypeError: print()
**Error**: 
```py
'something' is an invalid keyword argument for print()
```
Here `something` can be anything!

**Solution**:

This means that there is an Argument in `print` function which doesn't exists in your code. Your code might be like this:
```py
print(something="hi")
```
#### Arguments for `print` function
| Argument | Description |
| :--: | :-- |
| \*objects| an object/objects to be printed. |
| sep | the separator between multiple printed objects. |
| end | the character/string printed at the end after the object. |
| file | specifies the file where the output goes. By default this is the console. |
| flush | flushes the stream/file forcibly if set `True` |

Source: [Python Documentation](https://docs.python.org/3/library/functions.html#print)
