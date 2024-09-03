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
    - [Assignment Operators](#assignment-operators)
    - [Arithmetic Operations](#arithmetic-operations)

## Variables

- A variable is like a labelled box where you can store data.

- You start by writing the variable's name (**Declaration**), then you write an equals sign (`=`), then you write the value (**Initialization**).

- The value can almost anything, such as a string, a number, arithmetic operations, function calls, other variables, and more.

- The variable's name is always written with no quotation marks.

- There are many `case` formats you can use to write variable names that have multiple words, such as `camelCase`, `snake_case`, `kebab-case`, `PascalCase`, `alllowercase`, `ALLUPPERCASE`, `UPPER_CASE_CONSTANT` (typically used for constants), and more. These formats make the code more readable.

- When a variable already has a value, you can overwrite the value with something else.

- When printing a variable, you do not use quotation marks (`" "`), just the variable's name. This will print out the variable's value.

- Other languages use keywords (`int, string, double`, etc.) to denote what type the variable will be, such as `int variableName = valueHere;` in C# denotes an integer variable. Python does not use these keywords because it is an ambiguously typed language.

- You can assign multiple values to multiple variables (one value per variable) in one line. If the number of values does not match (less or more) the number of variables, Python will say `ValueError: not enough values to unpack` or `ValueError: too many values to unpack`.

- You can assign one value to multiple variables in one line.

- Rules for Python variable names:
  
  - A variable name can only contain alphabets, numbers and underscores (ie. A-Z, a-z, 0-9, and _).
  
  - A variable name cannot start with a number, but a number can be anywhere else in the name. (Wrong: `1variable`, Right: `variable1`)
  
  - A variable name cannot have spaces in between. (Wrong: `variable name`, Right: `variableName`)
  
  - Variable names are case-sensitive (age, Age, aGe, agE, AGe, aGE, AgE, and AGE are all different variables).

- Continue to [Datatype](#datatype) to see the different types of variables.

- If you have a collection of values in a list, tuple etc. Python allows you to extract the values into variables. This is called `unpacking`.

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

# Multiple Values to Multiple Variables
x, y, z = "Orange", "Banana", "Cherry"
print(x) # Output: Orange
print(y) # Output: Banana
print(z) # Output: Cherry

# One Value to Multiple Variables
x = y = z = "Orange"
print(x) # Output: Orange
print(y) # Output: Orange
print(z) # Output: Orange

# Unpacking
fruits = ["Apple", "Banana", "Cherry"]
x, y, z = fruits
print(x) # Output: Apple
print(y) # Output: Banana
print(z) # Output: Cherry

# ----------- End of Variables Code Block ----------- #
```

## Datatype

- The `datatype`, or more often just called `type`, of a variable is defined by the kind of value it stores. As explained in the [Variables](#variables) section: some languages, like C#, are "typed" languages which means they hard-define what type the variable will be.

- Typed variables can be overwritten by new values of the same type, but cannot be overwritten by new values of a different type unless you manually change the type (Python is ambiguously typed so we won't go over manual type changing here)

- Python is `ambiguously typed` or `typeless` (depending on who you ask), which means you do not hard-define the variable's type, rather the compiler infers the variable's type based on what value the variable stores.

- Typeless is powerful because you don't have to worry about manually declaring the type or manually changing the type.

- Typeless also has a drawback because it is not type-protected which means a variable can be overwritten by any value type, even if it is not intended to ever be a different type. This can cause bugs that are only caught in runtime.

- If you want to specify the data type of a variable, this can be done with `casting`. Casting does not cause the variable to stay that type though, you can still overwrite the variable to a different type with a normal variable assignment.

- You can get the type of a variable with the `type()` function.

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

# Casting
x = str(3)    # x will be "3" (string)
y = int(3)    # y will be 3 (integer)
z = float(3)  # z will be 3.0 (float)
x = 5         # x will change to 5 (integer)

# Get Type
x = 5
y = "John"
print(type(x)) # Output: <class 'int'>
print(type(y)) # Output: <class 'str'>
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

### Assignment Operators

- The Basic Assignment Operator is the single equals sign (`=`) and this assigns the value on its right to the variable on its left.

- Compound Assignment Operators combine arithmetic operations with assignment. They are a shorthand way of performing operations on a variable & assigning the result back to the variable.

- Compound Assignment Operators modify the actual variable itself so if you want leave that variable alone, you need to use a regular [Arithmetic Operation](#arithmetic-operations) that performs a math equation & assigns the result to a new variable.

```python
# ----------- Assignment Operators Code Block ----------- #

# Basic Assignment Operator:
length = 15

# Without Compound Assignment Operators:
length = 15
length = length + 5 # Updates length by adding 5 to its current value
print(length)  # Output: 20

# Using Compound Assignment Operators:
length = 15
length += 5  # Shorthand for length = length + 5
print(length)  # Output: 20

# We can use any other operator in the same way:
x -= 5  # Subtracts 5 from `x` and assigns the result back to `x`
x *= 3  # Multiplies `x` by 3 and assigns the result back to `x`
x /= 3  # Divides `x` by 3 and assigns the result back to `x`)
x %= 3  # Finds the remainder when `x` is divided by 3 and assigns the result back to `x`

# ----------- End of Assignment Operators Code Block ----------- #
```

### Arithmetic Operations

- Mathematical/Arithmetic operations can be done inside of `print()` statements or inside of a variable assignment with any operator. There must be no quote marks, for if there is then it's treated as a string.

```python
# ----------- Arithmetic Operations Code Block ----------- #

# Without quotes: The expression is evaluated, and the result is printed:
print(2 + 4) # Output: 6

# With quotes: The expression is treated as text (a string) and printed as is:
print("2 + 4") # Output: 2 + 4

a = 6
b = 3
print(a + b)  # Output: 9
print(a * b)  # Output: 18
print(a / b)  # Output: 2.0
# Integer Division (//) divides the numbers & returns a whole number, discarding the remainder
result = 10 // 3 # Output: 3 : 10 / 3 = 3.333.... & 0.333... is dropped.

# Modulo (%) returns the remainder of a division
print(a % b) # Output: 0 : No remainder from 6 / 3

# Exponent (**) raises a number to the power of another number.
print(a ** b)  # Output: 216 : 6 to the power of 3 is 216 (6 * 6 * 6)

# Variable Assignment
age = 45 + 23
print(age) # Output: 68
c = a + b
print(c) # Output: 9

# ----------- End of Arithmetic Operations Code Block ----------- #
```
