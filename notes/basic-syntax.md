![Python Logo](/images/python-logo.png)

# Basic Syntax of Python

## Table of Contents

- [Basic Syntax of Python](#basic-syntax-of-python)
  - [Table of Contents](#table-of-contents)
  - [Print Statement](#print-statement)
    - [Formatted String Literals (F-Strings)](#formatted-string-literals-f-strings)
  - [Comments](#comments)
  - [Variables](#variables)
    - [Assignment Operators](#assignment-operators)
    - [Arithmetic Operations](#arithmetic-operations)
  - [Types](#types)
  - [String Variables](#string-variables)
    - [String Functions](#string-functions)
    - [String Repetition](#string-repetition)

## Print Statement

The `print()` statement is used to display output on the screen, such as numbers, text, or results of expressions.

- The basic syntax of a `print()` statement is `print(input here)`.
- Other languages require a semicolon (`;`) at the end of each line, but Python does not use semicolons.
- Numbers can be entered in the `print()` statement without quotes & it will print fine.
- Text has to be entered in the `print()` statement with either double quotes (`" "`) or single quotes (`' '`).
- To print text on multiple lines, you need to put a separate `print()` statement on separate lines for how many you want to print.
- To print multiple items on one single line, you will separate the items with commas. You can print items of different types (i.e. text, numbers, etc.) together.
- Adding one or more lines between two print statements does not affect the output. They will always only print on two lines.
- When printing an numeric variable, you can perform [Arithmetic Operations](#arithmetic-operations) on the variable inside the `print()` statement.
- String concatenation will explained in the [String Variables](#string-variables) section.
- If you try to add variables together of different types, it will throw an error. Exact error depends what you are trying to add.

```python
# ----------- Print Statements Code Block ----------- #

print(123) # Output: 123
print("I love Python") # Output: I love Python
print('I love Python') # Output: I love Python
print("I love Python", 1 + 2, "Yay") # Output: I love Python 3 Yay
firstAge = 25
secondAge = 50
print(firstAge + 5) # Output: 30
print(secondAge + 5) # Output: 55
print(firstAge + secondAge) # Output: 75
print("This is " + "a " + "combined string") # Output: This is a combined string
print("string" + 25) # TypeError: can only concatenate str (not "int") to str

# ----------- End of Print Statements Code Block ----------- #

```

### Formatted String Literals (F-Strings)

- **Formatted String Literals (F-Strings)** simplifies string formatting by making one single large string where you dynamically insert variables into the string using curly brackets (`{ }`).
- This is more readable and it's powerful because it allows for type-insensitive concatenation, such as strings with integers. F-Strings do this by converting everything inside of the F-String into a regular string, then it concatenates everything.
- F-Strings also keeps spaces within the large string so you don't have to make a separate space string (`" "`).
- F-Strings are commonly used in `print()` statements, but they can also be used within variable declarations.
- F-Strings are a good alternative to [Concatenation](#string-variables) which uses the addition operator (`+`) to combine variables together. This is good, but sometimes can be hard to read, and you have to make sure you add spaces inside of the string. Also, concatenatation does not allow combining items of different types.

```python
# ----------- F-Strings Code Block ----------- #

first-name = "John"
last-name = "Smith"
age = 45
concat-string = first-name + " " + last-name
f-string = f"My name is {first-name} {last-name} and I am {age} years old."

# Concatenation
print(first-name + " " + last_name) # Output: John Smith
print(concat-string) # Output: John Smith
rint("My name is " + first-name + " " + last_name) # Output: My name is John Smith
print("My name is " + first-name + " " + last_name + " and I am " + int1 + " years old.") # Output: TypeError: can only concatenate str (not "int") to str

# F-String
print(f"My name is {first-name} {last-name} and I am {age} years old.") # Output: My name is John Smith and I am 45 years old.
print(f-string) # Output: My name is John Smith and I am 45 years old.

# ----------- End of F-Strings Code Block ----------- #
```

## Comments

- Comments are special because they are used for taking notes, explaining a function, and other things that should not be run as code: `# This is a comment`
- Comments in Python start with a `#` and the program ignores everything after the `#`.
- A comment does not have to be text that explains the code, it can also be used to prevent Python from executing code.

```python
# ----------- Comments Code Block ----------- #

#print("Hello, World!")

print("Cheers, Mate!") # The print statement runs as normal, but the rest of this line is ignored.

# This is a
# multi-line
# comment

# ----------- End of Comments Code Block ----------- #
```

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
  - A variable name cannot start with a number. (Wrong: `1variable`, Right: `variable1`)
  - A variable name cannot have spaces in between. (Wrong: `variable name`, Right: `variableName`)
  - Variable names are case-sensitive (age, Age, and AGE are three different variables).
- Continue to [Types](#types) to see the different types of variables.

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

Mathematical/Arithmetic operations can be done inside of `print()` statements or inside of a variable assignment with any operator. There must be no quote marks, for if there is then it's treated as a string.

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

## Types

- The `type` of a variable is defined by the kind of value it stores. As explained in the [Variables](#variables) section: some languages, like C#, are "typed" languages which means they hard-define what type the variable will be.
- Typed variables can be overwritten by new values of the same type, but cannot be overwritten by new values of a different type unless you manually change the type (Python is ambiguously typed so we won't go over manual type changing here)
- Python is `ambiguously typed` or `typeless` (depending on who you ask), which means you do not hard-define the variable's type, rather the compiler infers the variable's type based on what value the variable stores.
- Typeless is powerful because you don't have to worry about manually declaring the type or manually changing the type.
- Typeless also has a drawback because it is not type-protected which means a variable can be overwritten by any value type, even if it is not intended to ever be a different type. This can cause bugs that are only caught in runtime.

```python
# ----------- Types Code Block ----------- #

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

# ----------- End of Types Code Block ----------- #
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
