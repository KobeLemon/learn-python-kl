![Python Logo](/images/python-logo.png)

# Conditional Statements

## Table of Contents

- [Conditional Statements](#conditional-statements)
  - [Table of Contents](#table-of-contents)
  - [If Else Statements](#if-else-statements)
  - [Conditional and Logical Operators](#conditional-and-logical-operators)

## If Else Statements

- Conditional Statements are used for decision making & comparing the values of multiple items. These items can be variables, raw strings, numbers, booleans, artithmetic, and almost anything else that can be compared to something else.

- It is always best to have at least an `if` and an `else` statement. You can add an `elif` statement (means else if) if you need multiple outcomes, but it's not required. An `else` statement is also not "required", but it's best to have one to make sure all possibilities are handled.

- You can have if statements inside if statements, this is called `nested if statements`.

- `if` statements cannot be empty, but if you for some reason have an `if` statement with no content, put in the `pass` statement to avoid getting an error.

- `If/Elif/Else` statements use indentation to know what code is inside of the statement. They also use a colon (`:`) to indicate the end of the condition.

- There are four main ways to write if/else statements:
  1. `If/Else`: Two possiblities. When the `if` statement is met, its code will run. For all other results, the `else` statement's code will run.

  2. `If/Elif.../Else`: Three or more possiblities. When the `if` statement is met, its code will run. You can chain as many `elif` statements as needed. The program will equate them from top to bottom & run only the statement that is met. For all other results, the `else` statement's code will run.

  3. For #3 & #4, you can write those same chains except you omit the `else` statement. These are useful if you want the `if` or `elif` statements to run their course & then continue the program after the conditional statement chain. If you want the `if` or `elif` statements to not run if they are not met & you want other code to run instead, you should use an `else` statement. Not using an `else` statement technically works, but it's not as readable & can cause issues if you only want one conditional statement to run.

```python
# ----------- If Else Statements Code Block ----------- #

# Basic Syntax
if condition:
    # code to run if the first condition is true
elif:
    # code to run if the second condition is true
# You can add as many elif statements as needed
else:
    # code to run if all above conditions are false

# If/Else Statement
a = 4
b = 5
if a == b:
    print("a and b are equal")
else:
    print("a and b are not equal") # a & b are not equal, so the else statement runs.

#If/Elif/Else Statement
grade = "A"

if grade == "A" or grade== "B":
    print("Great job!") # grade is "A" so only this statement will run.
elif grade == "C" or grade== "D":
    print("Good job, but you can do better!")
elif grade == "F":
    print("Sorry! Try again next year")
else:
    print("Invalid grade!")

# Nested If Statements
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")

# Empty If Statement
if b > a:
  pass

# ----------- End of If Else Statements Code Block ----------- #
```

## Conditional and Logical Operators

- Conditional operators compare two values to each other & returns a boolean true or false.

- After two conditional operators return their booleans, Logical operators are used to compare those two booleans.

- Conditional & Logical operators can be used together to compare multiple different equations together.

- When using the Equals (`==`) operator, you always need to use two equals signs. If you only use one equals sign, that is the assignment operator which just overwrites the variable with the value you were intending to compare it with.

- There are 6 main conditional operators:
  
  - Equals: `a == b`
  
  - Not Equals: `a != b`
  
  - Less than: `a < b`
  
  - Less than or equal to: `a <= b`
  
  - Greater than: `a > b`
  
  - Greater than or equal to: `a >= b`

- There are three main logical operators:
  
  - `and` - checks if both of the two conditions are true. This ensures the conditional statement is only ran when both conditions are true. If the first condition is true, the second condition is also computed.
  
  - `or` - checks if only one of the two conditions are true. It only matters if one or more conditions are true. If the first condition is true, the second condition is not computed. If the first condition is false, then the second condition is computed.
  
  - `not` - reverses the result of the conditional statement. If the conditional statement is false instead of true, then that statement's code runs. Typically it is more readable to just use the opposite conditional operator. E.g. `a != b` instead of `if not a == b`.

```python
# ----------- Conditional and Logical Operators Code Block ----------- #
a = 200
b = 33
c = 500

# AND
if a > b and c > a:
  print("Both conditions are True")

# OR
if a > b or a > c:
  print("At least one of the conditions is True")

# NOT
if not a > b:
  print("a is NOT greater than b")

# ----------- End of Conditional and Logical Operators Code Block ----------- #
```
