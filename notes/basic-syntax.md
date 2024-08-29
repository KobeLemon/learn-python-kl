![Python Logo](/images/python-logo.png)

# Print Statements & Comments

## Table of Contents

- [Print Statements \& Comments](#print-statements--comments)
  - [Table of Contents](#table-of-contents)
  - [Print Statement](#print-statement)
    - [Formatted String Literals (F-Strings)](#formatted-string-literals-f-strings)
    - [Assignment Operators](#assignment-operators)
    - [Arithmetic Operations](#arithmetic-operations)
  - [Comments](#comments)

## Print Statement

The `print()` statement is used to display output on the screen, such as numbers, text, or results of expressions.

- The basic syntax of a `print()` statement is `print(input here)`.

- Other languages require a semicolon (`;`) at the end of each line, but Python does not use semicolons.

- Numbers can be entered in the `print()` statement without quotes & it will print fine.

- Text has to be entered in the `print()` statement with either double quotes (`" "`) or single quotes (`' '`).

- To print text on multiple lines, you need to put a separate `print()` statement on separate lines for how many you want to print.

- To print multiple items on one single line, you will separate the items with commas. You can print items of different types (i.e. text, numbers, etc.) together. Commas automatically adds a space between the items, so you do not need to add spaces to the items.

- Adding one or more lines between two print statements does not affect the output. They will always only print on two lines.

- When printing an numeric variable, you can perform [Arithmetic Operations](#arithmetic-operations) on the variable inside the `print()` statement.

- String concatenation will explained in the [String Variables](/notes/types-variables.md/#variables) section of [types-variables.md](/notes/types-variables.md).

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

- F-Strings are a good alternative to Concatenation which uses the addition operator (`+`) to combine variables together. This is good, but sometimes can be hard to read, and you have to make sure you add spaces inside of the string. Also, concatenatation does not allow combining items of different types.

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
