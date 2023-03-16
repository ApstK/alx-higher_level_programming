0x04. Python - More Data Structures: Set, Dictionary

Dictionaries are sometimes found in other languages as “associative memories” or “associative arrays”. Unlike sequences, which are indexed by a range of numbers, dictionaries are indexed by keys, which can be any immutable type; strings and numbers can always be keys. Tuples can be used as keys if they contain only strings, numbers, or tuples; if a tuple contains any mutable object either directly or indirectly, it cannot be used as a key. You can’t use lists as keys, since lists can be modified in place using index assignments, slice assignments, or methods like append() and extend().

It is best to think of a dictionary as a set of key: value pairs, with the requirement that the keys are unique (within one dictionary). A pair of braces creates an empty dictionary: {}. Placing a comma-separated list of key:value pairs within the braces adds initial key:value pairs to the dictionary; this is also the way dictionaries are written on output.

The main operations on a dictionary are storing a value with some key and extracting the value given the key. It is also possible to delete a key:value pair with del. If you store using a key that is already in use, the old value associated with that key is forgotten. It is an error to extract a value using a non-existent key.

Performing list(d) on a dictionary returns a list of all the keys used in the dictionary, in insertion order (if you want it sorted, just use sorted(d) instead). To check whether a single key is in the dictionary, use the in keyword.

The operators in and not in test for membership. x in s evaluates to True if x is a member of s, and False otherwise. x not in s returns the negation of x in s. All built-in sequences and set types support this as well as dictionary, for which in tests whether the dictionary has a given key. For container types such as list, tuple, set, frozenset, dict, or collections.deque, the expression x in y is equivalent to any(x is e or x == e for e in y).

For the string and bytes types, x in y is True if and only if x is a substring of y. An equivalent test is y.find(x) != -1. Empty strings are always considered to be a substring of any other string, so "" in "abc" will return True.

For user-defined classes which define the __contains__() method, x in y returns True if y.__contains__(x) returns a true value, and False otherwise.

For user-defined classes which do not define __contains__() but do define __iter__(), x in y is True if some value z, for which the expression x is z or x == z is true, is produced while iterating over y. If an exception is raised during the iteration, it is as if in raised that exception.

Lastly, the old-style iteration protocol is tried: if a class defines __getitem__(), x in y is True if and only if there is a non-negative integer index i such that x is y[i] or x == y[i], and no lower integer index raises the IndexError exception. (If any other exception is raised, it is as if in raised that exception).

The operator not in is defined to have the inverse truth value of in.
