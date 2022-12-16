## TypeError
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

**Solve**:

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
