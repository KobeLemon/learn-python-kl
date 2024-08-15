![Python Logo](/images/python-logo.png)

# Basic Syntax of Python

## Table of Contents

- [Basic Syntax of Python](#basic-syntax-of-python)
  - [Table of Contents](#table-of-contents)
  - [Print Statement](#print-statement)
  - [Arithmetic Operations](#arithmetic-operations)
  - [Comments](#comments)
  - [Variables](#variables)
    - [Assignment Operators](#assignment-operators)
  - [String Variables](#string-variables)
    - [String Functions](#string-functions)
  - [Types](#types)
  - [String Repetition](#string-repetition)

## Print Statement

The `print()` statement is used to display output on the screen, such as numbers, text, or results of expressions.

- The basic syntax of a `print()` statement is `print(input here)`.
- Other languages require a semicolon (`;`) at the end of each line, but Python does not use semicolons.
- Numbers can be entered in the `print()` statement without quotes & it will print fine.
- Text has to be entered in the `print()` statement with either double quotes (`" "`) or single quotes (`' '`).
- To print text on multiple lines, you need to put a separate `print()` statement on separate lines for how many you want to print.
- To print multiple items on one single line, you will separate the items with commas. You can print items of different types (i.e. text, numbers, etc.) together.
- Adding one or multiple lines between two print statements does not affect the output. They will always only print on two lines.
- When printing an numeric variable, you can perform arithmetic operations on the variable inside the `print()` statement.
- If you try to add multiple strings together in a print statement, it will concatenate (combine) them into one string & then print the new string. It will only add spaces if they exist in the string(s), so you may need to add extra spaces (quote marks with a space in between, `" "`) where needed.
- If you try to add variables together of different types, it will throw an error. Exact error depends what you are trying to add.

```python
# -----------Print Statements Code Block---------------- #

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

# -----------End of Print Statements Code Block---------------- #

```

## Arithmetic Operations

Mathematical/Arithmetic operations can be done inside of `print()` statements or inside of a variable assignment with any operator. There must be no quote marks, for if there is then it's treated as a string.

```python
# -----------Arithmetic Operations Code Block---------------- #

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

# -----------End of Arithmetic Operations Code Block---------------- #
```

## Comments

- Comments are special because they are used for taking notes, explaining a function, and other things that should not be run as code: `# This is a comment`
- Comments in Python start with a `#` and the program ignores everything after the `#`.
- A comment does not have to be text that explains the code, it can also be used to prevent Python from executing code.

```python
# -----------Comments Code Block---------------- #

#print("Hello, World!")

print("Cheers, Mate!") # The print statement runs as normal, but the rest of this line is ignored.

# This is a
# multi-line
# comment

# -----------End of Comments Code Block---------------- #
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
# -----------Variables Code Block---------------- #

# Regular Declare/Initialize
age = 25
print(age) # Output: 25

# Overwrite the variable
age = 25
print(age) # Output: 25
age = 89
print(age) # Output: 89

# -----------End of Variables Code Block---------------- #
```

### Assignment Operators

- The Basic Assignment Operator is the single equals sign (`=`) and this assigns the value on its right to the variable on its left.
- Compound Assignment Operators combine arithmetic operations with assignment. They are a shorthand way of performing operations on a variable & assigning the result back to the variable.

```python
# -----------Assignment Operators Code Block---------------- #
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

# -----------End of Assignment Operators Code Block---------------- #
```

## String Variables

- 

### String Functions

- `len(string)`: returns the length of the string

```python
# -----------String Variables/Functions Code Block---------------- #

CODEHERE

# -----------End of String Variables/Functions Code Block---------------- #
```

## Types

- The `type` of a variable is defined by the kind of value it stores. As explained in the [Variables](#variables) section: some languages, like C#, are "typed" languages which means they hard-define what type the variable will be.
- Typed variables can be overwritten by new values of the same type, but cannot be overwritten by new values of a different type unless you manually change the type (Python is ambiguously typed so we won't go over manual type changing here)
- Python is `ambiguously typed` or `typeless` (depending on who you ask), which means you do not hard-define the variable's type, rather the compiler infers the variable's type based on what value the variable stores.
- Typeless is powerful because you don't have to worry about manually declaring the type or manually changing the type.
- Typeless also has a drawback because it is not type-protected which means a variable can be overwritten by any value type, even if it is not intended to ever be a different type. This can cause bugs that are only caught in runtime.

```python
# -----------Types Code Block---------------- #

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

# -----------End of Types Code Block---------------- #
```

## String Repetition

- You can multiply (`*`) strings to create a new string that repeats the original string a certain number of times. This technique is known as string repetition or string replication.
- You can do the following:
  1) Create a new variable & then assign a repeated variable to it, then print or do other things with that new variable.
  2) Use the repetition operator inside of a print statement, function call, etc.
  3) Put the plain string into the print statement, function call, etc. & then multiply the string directly.

```python
# -----------String Repetition Code Block---------------- #

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

# -----------End of String Repetition Code Block---------------- #
```
