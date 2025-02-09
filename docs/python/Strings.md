# Strings 

## Type Hinting 

my_str : str

- String consist of single characters and are sequential data types.

- Due Sequential in nature  which is why many actions can be performed analogously, such as slicing.

- Python does not have a data type for inividual characters, so they are simply represented as string of length 1.

- Strings can be created as character sequences in double or single quotes, as shown by the following two lines:

`str1 = "DOUBLE QUOTED STRING"`

`str2 = 'SINGLE QUOTED STRING'`


## Most Common functions that are useful in practice

- **len(str)**: gets the length of the string. This is a general Python function for querying the length of sequential data types such as lists or tuples, etc., but also strings.


- **str[index]**: provides index-based access to individual letters.
- **str[start:end]/ str[start:end:step]**: extracts characters between position start and end-1. for stepwidth can be specified. [::-1] will result in a new string with reverse letter order of the original string.
- **str[:end]** : extracts the characters between the beginning and the position end - 1.
- **str[start:]**: extracts the characters between the position start and the end of the string.
- **str.lower()/str.upper()** : creates a new string consisting of lowercase or uppercase letters. Numbers and punctuation marks are not converted.
- **str.strip()** : removes whitespace at the beginning and end of text and returns this as a new string. As a special feature, you can pass a character that will be removed instead of whitespace.
- **str.isalpha()/str.isdigit()/...** :  checks if all characters of the string are alphanumeric, digits, etc.
- **str.startswith(other)/str.endswith(other)** : checks whether the string starts or ends with the given string.
- **str.find(other)/str.rfind(other)** : searches for the supplied string and returns the index of the first occurrence or -1 on nonexistence. The function rfind() searches from the end. As a special feature, it is possible to specify an index range in both cases.
- **str.index(other, start, end)/str.rindex(other, start, end)**: returns the index of the first or last occurrence of other. Unlike find(), an exception is thrown if the index is not present.
- **str.count(text)** :counts how many times text occurs in the string.
- **str.replace(old, new)** creates a new string in which all occurrences of old are replaced by new.
- **str.split(delim)** : returns a list of substrings resulting from splitting the original string. The delimiter is no regular expression1. Without specifying a delimiter, a text is split with respect to whitespace.
- **str.join(list)** :  does the opposite of split(). Specifically, the elements passed as a list are joined to the string as a delimiter.
- **str.capitalize()/str.title()** : converts the first character to uppercase. With title() additionally within a string, the beginning
of each new word is converted to uppercase.


### Examples 

```python
# Index-Based Access
text = "Python"
print(text[0])  # Output: P
print(text[-1]) # Output: n


# Slicing String

text = "Hello, World!"
print(text[0:5])    # Output: Hello
print(text[:5])     # Output: Hello
print(text[7:])     # Output: World!
print(text[::-1])   # Output: !dlroW ,olleH
print(text[::2])    # Output: Hlo ol!

# Case Conversion

text = "Python"
print(text.lower())  # Output: python
print(text.upper())  # Output: PYTHON

# Removing Whitspace

text = "  Hello  "
print(text.strip())     # Output: "Hello"
print(text.strip(" H")) # Output: "ello  "


# Checking String Content

text = "Python123"
print(text.isalpha())  # Output: False
print(text.isdigit())  # Output: False
print("123".isdigit()) # Output: True

# Checking Start/End of a string 

text = "hello.py"
print(text.startswith("hello"))  # Output: True
print(text.endswith(".py"))      # Output: True


# Finding and Indexing 

text = "hello world"
print(text.find("o"))   # Output: 4
print(text.rfind("o"))  # Output: 7
print(text.index("o"))  # Output: 4
print(text.index("z")) # Raises ValueError

# Counting Occurence

text = "banana"
print(text.count("a"))  # Output: 3

# Replacing Substrings

text = "hello world"
print(text.replace("world", "Python"))  # Output: hello Python

# Splitting and Joining Strings

text = "apple,banana,orange"
words = text.split(",")
print(words)  # Output: ['apple', 'banana', 'orange']

separator = " - "
joined_text = separator.join(words)
print(joined_text)  # Output: apple - banana - orange

# Capitalization and Title Case 

text = "hello world"
print(text.capitalize()) # Output: Hello world
print(text.title())      # Output: Hello World

```

