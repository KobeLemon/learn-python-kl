![Python Logo](/images/python-logo.png)

# User Inputs

## Table of Contents

- [User Inputs](#user-inputs)
  - [Table of Contents](#table-of-contents)
  - [User Input](#user-input)

## User Input

- Hard coding values into variables is often necessary, but often you may need a user's input, especially with things such as forms, games, to do lists, etc.

- The `input()` function can be used to pause the program and ask the user for input, then their input will be stores into a variable, then that variable can be used later. Once the user gives their input, the program continues.

- `input()` by default stores the user input as a string so if you want the user to enter a different datatype, such as a number, you can convert it to use that type with this syntax: `type(input())`.

- For example: if you have two `int(input())` statements & the user enters 2 for the first & and 3 for the second, then you add those two, the output will be 5. However, if you don't convert it to an integer, the output will be 23 because `input()` would take the input as a string, string concatenation will be performed instead of integer addition.

- As with most functions, you can technically use the `input()` function inside of a variable declaration, function call, or print statement. Though it is best to only use `input()` in a variable declaration & then use that variable in the PR or FC. Using `input()` in an PR or FC is not good practice because it's not readable and makes it harder to understand what the program is using `input()` for.

- Once the user's input is stored into the variable, it becomes a regular variable & can be used as such.

- `input()` only allows one single input, but sometimes you need to accept multiple inputs in a single line. For this you can use the `input().split()` function modifier.

- `.split()` breaks this single line of input into multiple parts based on spaces in the user's input. In other words, each separate word separated by a space is treated as an independent input & stored in different variable.

- If you need to take multiple integer inputs, `int()` only works on a single item so you will need to convert them separately. To handle this, you can use the `map()` function to convert the split inputs to integers in one step. We will go more in depth with `map()` in a later section. This is the syntax: `a, b, c = map(int, input().split())`

- That syntax takes the list of multiple string inputs, then applies the `int()` function to each input to convert each one into an integer.

```python
# ----------- User Input Code Block ----------- #

# String User Input
string = input() # Input: Hello World!
print(string) # Output: Hello World!

# Int User Input
number = int(input()) # Input: 12
print(number) # Output: 12

# Split Input
a, b, c, d = input().split() # Input: Air Water Earth Fire
print(d) # Output: Fire
print(c) # Output: Earth
print(b) # Output: Water
print(a) # Output: Air

# map() int split
a, b, c = map(int, input().split()) # Input: 1 2 3
print(a + b + c) # Output: 6

# ----------- User Input Code Block ----------- #
```
