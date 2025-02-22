# Interview Question in Python 

- **1. What is mutable and immutable objects/data types in Python?**

Mutation generally refers to change. So when we say an object is mutable or immutable we meant to say that value of object can/cannot change.




- **2. What is the purpose of the single underscore “_” variable in Python?**

Python automatically stores the value of last expression in  interpreter in single underscore.
```Python

>>> 78 + 89
167
>>> _
167
```
Single underscore used in unpacking to ignore value(s).

```Python
>>> a, _, b = (1, 12, 2)
>>> a, *_, b = (1, 12, 13, 14, 15, 16, 2) # only want first and last value
>>> a, *x, b = (1, 12, 13, 14, 15, 16, 2) # note that any other name can also be used
>>> _ # returns a list of elements
[12, 13, 14, 15, 16]
```
True