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
