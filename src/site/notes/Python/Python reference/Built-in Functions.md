---
{"dg-publish":true,"permalink":"/python/python-reference/built-in-functions/","created":"","updated":""}
---

[Built-in Functions](https://realpython.com/python-data-types/#built-in-functions)

| Function                                                                                            | Description                                                                     |
|:--------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Type conversion**                                                                                 |                                                                                 |
| ascii()                                                                                             | Returns a string containing a printable representation of an object             |
| bin()                                                                                               | Converts an integer to a binary string                                          |
| bool()                                                                                              | Converts an argument to a Boolean value                                         |
| chr()                                                                                               | Returns string representation of character given by integer argument            |
| complex()                                                                                           | Returns a complex number constructed from arguments                             |
| float()                                                                                             | Returns a floating-point object constructed from a number or string             |
| hex()                                                                                               | Converts an integer to a hexadecimal string                                     |
| int()                                                                                               | Returns an integer object constructed from a number or string                   |
| oct()                                                                                               | Converts an integer to an octal string                                          |
| ord()                                                                                               | Returns integer representation of a character                                   |
| repr()                                                                                              | Returns a string containing a printable representation of an object             |
| str()                                                                                               | Returns a string version of an object                                           |
| type()                                                                                              | Returns the type of an object or creates a new type object                      |
| **Iterables and Iterators**                                                                         |                                                                                 |
| [all()](https://realpython.com/python-all/)                                                         | Returns True if all elements of an iterable are true                            |
| [any()](https://realpython.com/any-python/)                                                         | Returns True if any elements of an iterable are true                            |
| [enumerate()](https://realpython.com/python-enumerate/)                                             | Returns a list of tuples containing indices and values from an iterable         |
| filter()                                                                                            | Filters elements from an iterable                                               |
| iter()                                                                                              | Returns an iterator object                                                      |
| [len()](https://realpython.com/len-python-function/)                                                | Returns the length of an object                                                 |
| [map()](https://realpython.com/python-map-function/)                                                | Applies a function to every item of an iterable                                 |
| next()                                                                                              | Retrieves the next item from an iterator                                        |
| [range()](https://realpython.com/python-range/)                                                     | Generates a range of integer values                                             |
| reversed()                                                                                          | Returns a reverse iterator                                                      |
| slice()                                                                                             | Returns a slice object                                                          |
| [sorted()](https://realpython.com/python-sort/)                                                     | Returns a sorted list from an iterable                                          |
| [zip()](https://realpython.com/python-zip-function/)                                                | Creates an iterator that aggregates elements from iterables                     |
| **Math**                                                                                            |                                                                                 |
| [abs()](https://realpython.com/python-absolute-value/#using-the-built-in-abs-function-with-numbers) | Returns absolute value of a number                                              |
| divmod()                                                                                            | Returns quotient and remainder of integer division                              |
| [max()](https://realpython.com/python-min-and-max/)                                                 | Returns the largest of the given arguments or items in an iterable              |
| [min()](https://realpython.com/python-min-and-max/)                                                 | Returns the smallest of the given arguments or items in an iterable             |
| pow()                                                                                               | Raises a number to a power                                                      |
| round()                                                                                             | Rounds a floating-point value                                                   |
| [sum()](https://realpython.com/python-sum-function/)                                                | Sums the items of an iterable                                                   |
| **Composite Data Type**                                                                             |                                                                                 |
| bytearray()                                                                                         | Creates and returns an object of the bytearray class                            |
| bytes()                                                                                             | Creates and returns a bytes object (similar to bytearray, but immutable)        |
| dict()                                                                                              | Creates a dict object                                                           |
| frozenset()                                                                                         | Creates a frozenset object                                                      |
| list()                                                                                              | Creates a list object                                                           |
| object()                                                                                            | Creates a new featureless object                                                |
| set()                                                                                               | Creates a set object                                                            |
| tuple()                                                                                             | Creates a tuple object                                                          |
| **Classes, Attributes, and Inheritance**                                                            |                                                                                 |
| classmethod()                                                                                       | Returns a class method for a function                                           |
| delattr()                                                                                           | Deletes an attribute from an object                                             |
| getattr()                                                                                           | Returns the value of a named attribute of an object                             |
| hasattr()                                                                                           | Returns True if an object has a given attribute                                 |
| isinstance()                                                                                        | Determines whether an object is an instance of a given class                    |
| issubclass()                                                                                        | Determines whether a class is a subclass of a given class                       |
| property()                                                                                          | Returns a property value of a class                                             |
| setattr()                                                                                           | Sets the value of a named attribute of an object                                |
| [super()](https://realpython.com/python-super/)                                                     | Returns a proxy object that delegates method calls to a parent or sibling class |
| **Input/Output**                                                                                    |                                                                                 |
| format()                                                                                            | Converts a value to a formatted representation                                  |
| [input()](https://realpython.com/python-input-integer/)                                             | Reads input from the console                                                    |
| open()                                                                                              | Opens a file and returns a file object                                          |
| [print()](https://realpython.com/python-print/)                                                     | Prints to a text stream or the console                                          |
| **Variables, References, and Scope**                                                                |                                                                                 |
| dir()                                                                                               | Returns a list of names in current local scope or a list of object attributes   |
| globals()                                                                                           | Returns a dictionary representing the current global symbol table               |
| id()                                                                                                | Returns the identity of an object                                               |
| locals()                                                                                            | Updates and returns a dictionary representing current local symbol table        |
| vars()                                                                                              | Returns dict attribute for a module, class, or object                           |
| **Miscellaneous**                                                                                   |                                                                                 |
| callable()                                                                                          | Returns True if object appears callable                                         |
| compile()                                                                                           | Compiles source into a code or AST object                                       |
| [eval()](https://realpython.com/python-eval-function/)                                              | Evaluates a Python expression                                                   |
| [exec()](https://realpython.com/python-exec/)                                                       | Implements dynamic execution of Python code                                     |
| hash()                                                                                              | Returns the hash value of an object                                             |
| help()                                                                                              | Invokes the built-in help system                                                |
| memoryview()                                                                                        | Returns a memory view object                                                    |
| staticmethod()                                                                                      | Returns a static method for a function                                          |
| \_\_import\_\_()                                                                                    | Invoked by the import statement                                                 |
|                                                                                                     |                                                                                 |