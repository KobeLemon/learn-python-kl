![Python Logo](/images/python-logo.png)

# Datatypes & Variables

## Table of Contents

- [Datatypes \& Variables](#datatypes--variables)
  - [Table of Contents](#table-of-contents)
  - [Variables](#variables)
  - [Datatype](#datatype)
  - [String Variables](#string-variables)
    - [String Functions](#string-functions)
    - [String Repetition](#string-repetition)

## Variables

- A variable is like a labelled box where you can store data.

- You start by writing the variable's name (**Declaration**), then you write an equals sign (`=`), then you write the value (**Initialization**).

- The value can almost anything, such as a string, a number, arithmetic operations, function calls, other variables, and more.

- The variable's name is always written with no quotation marks.

- There are many `case` formats you can use to write variable names that have multiple words, such as `camelCase`, `snake_case`, `kebab-case`, `PascalCase`, `alllowercase`, `ALLUPPERCASE`, `UPPER_CASE_CONSTANT` (typically used for constants), and more. These formats make the code more readable.

- When a variable already has a value, you can overwrite the value with something else.

- When printing a variable, you do not use quotation marks (`" "`), just the variable's name. This will print out the variable's value.

- Other languages use keywords (`int, string, double`, etc.) to denote what type the variable will be, such as `int variableName = valueHere;` in C# denotes an integer variable. Python does not use these keywords because it is an ambiguously typed language.

- Rules for Python variable names:
  
  - A variable name can only contain alphabets, numbers and underscores (ie. A-Z, a-z, 0-9, and _).
  
  - A variable name cannot start with a number, but a number can be anywhere else in the name. (Wrong: `1variable`, Right: `variable1`)
  
  - A variable name cannot have spaces in between. (Wrong: `variable name`, Right: `variableName`)
  
  - Variable names are case-sensitive (age, Age, aGe, agE, AGe, aGE, AgE, and AGE are all different variables).

- Continue to [Datatype](#datatype) to see the different types of variables.

```python
# ----------- Variables Code Block ----------- #

# Regular Declare/Initialize
age = 25
print(age) # Output: 25

# Overwrite the variable
age = 25
print(age) # Output: 25
age = 89
print(age) # Output: 89

# ----------- End of Variables Code Block ----------- #
```

## Datatype

- The `datatype`, or more often just called `type`, of a variable is defined by the kind of value it stores. As explained in the [Variables](#variables) section: some languages, like C#, are "typed" languages which means they hard-define what type the variable will be.

- Typed variables can be overwritten by new values of the same type, but cannot be overwritten by new values of a different type unless you manually change the type (Python is ambiguously typed so we won't go over manual type changing here)

- Python is `ambiguously typed` or `typeless` (depending on who you ask), which means you do not hard-define the variable's type, rather the compiler infers the variable's type based on what value the variable stores.

- Typeless is powerful because you don't have to worry about manually declaring the type or manually changing the type.

- Typeless also has a drawback because it is not type-protected which means a variable can be overwritten by any value type, even if it is not intended to ever be a different type. This can cause bugs that are only caught in runtime.

```python
# ----------- Datatype Code Block ----------- #

# Numeric variables - hold integers and decimal values.
age = 25 # "int" type - whole numbers
temperature = 98.6 # "float" type - decimal numbers

# String variables - Stores a sequence of characters enclosed in single or double quotes.
name = "John Doe"
message = 'Hello, world!'

# Boolean variables - only hold the values true and false.
is_true = True
is_false = False

# List variables - Stores a collection of items, which can be of different types. Allows duplicates.
numbers = [1, 2, 3, 4, 5]
fruits = ["apple", "banana", "orange"]

# Tuple variables - A collection which is ordered and immutable (unchangeable). Allows duplicates.
coordinates = (10, 20)

# Dictionary variables - A key-value pair collection where one key matches one value. Keys are unique, but values can repeat.
person = {"name": "Alice", "age": 30, "height": 30}

# Set variables - A collection that cannot contain duplicate items, only unique items.
unique_numbers = {1, 2, 3}

# None variable - No value, just an empty variable.
empty_value = None

# ----------- End of Datatype Code Block ----------- #
```

## String Variables

- Strings are text variables surrounded by double quotes (`" "`) or single quotes (`' '`).

- You can use many helper functions to perform different operations on a string, such as getting the character length, changing the case, etc.

- You can use these functions in variable declarations, in function calls, in print statements, etc.

- If you try to add multiple strings together in a print statement, function call, variable declaration, etc, the strings will concatenate (combine) into one new string that can then be used. It will only add spaces if they exist in the string(s), so you may need to add extra spaces (quote marks with a space in between, `" "`) where needed.

### String Functions

- `len(string)`: returns the length of characters in a string

- `string.lower()`: returns the string with all characters changed to lower case

- `string.upper()`: returns the string with all characters changed to upper case

```python
# ----------- String Variables/Functions Code Block ----------- #

# len(string)
greeting = "hello"
len_string = len(greeting)
print(len_string) # Output: 8

# string.lower() & string.upper()
name = 'JohnSmith'
lowercase_name = name.lower()
uppercase_name = name.upper()
print(lowercase_name) # Output: johnsmith
print(uppercase_name) # Output: JOHNSMITH

# ----------- End of String Variables/Functions Code Block ----------- #
```

### String Repetition

- You can multiply (`*`) strings to create a new string that repeats the original string a certain number of times. This technique is known as string repetition or string replication.

- You can do the following:
  1) Create a new variable & then assign a repeated variable to it, then print or do other things with that new variable.
  2) Use the repetition operator inside of a print statement, function call, etc.
  3) Put the plain string into the print statement, function call, etc. & then multiply the string directly.

```python
# ----------- String Repetition Code Block ----------- #

# Option 1
string = "hello "
result = string * 3
print(result) # Output: hello hello hello

# Option 2
string = "bye "
print(string * 3) # Output: bye bye bye

# Option 3
print("sup " * 3) # Output: sup sup sup

# string is assigned the value `hello `
# result = string * 3 creates a new string by repeating `hello ` three times
# `hello hello hello ` is stored into the variable `result`, then `result` is printed.

# ----------- End of String Repetition Code Block ----------- #
```
