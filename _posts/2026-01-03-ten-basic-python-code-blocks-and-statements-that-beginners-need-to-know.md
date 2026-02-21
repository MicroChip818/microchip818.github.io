---
layout: posts
title: 10 basic Python code blocks and statements that beginners need to know
date: 2026-01-03 14:26:00 -0800
author: Ethan K.
categories: Overview
---
Python 3.14 contains a wide range of statements and code blocks (multiple statements used to perform similar tasks) that can be used to manipulate data. Here are 10 of them that every new Python programmer should know. I will provide examples for each.
## Tips
- Try running the following code blocks using the Python IDLE shell.
- For statements (single lines that have individual outputs), such as print and declaring a variable, run 1 line at a time.
- For code blocks, such as if statements and for loops, run the entire code block, enter into a new line, then create an extra line below.
- A hashtag (#) represents the start of a single-line comment in Python, used to leave developer notes. Comments are not part of the actual code.

## 1. print()

- This statement prints all kinds of data you want the console to display.
- It can range from text to complex variables!
- If you print text, wrap the text around quotation marks so it isn't seen as a variable.
```python
print("Code Outside the Box") # Output: Code Outside the Box
print(2026) # Output: 2026
print(1+2+3+4) # Output: 10
print([1, 2, 3, 4, 5]) # Output: [1, 2, 3, 4, 5]
```

## 2. var = 100

- The left side is the variable name, and the right side is the value.
- When printing a variable, place the variable's name in the print statement, and it will print the value of the variable.
- You may only use letters, numbers, and underscores to name a variable.
- A number cannot be the first character of a variable.
- The variable cannot be named as a Python keyword (examples: break, continue, True, False). You can find all Python keywords at <a href="https://www.w3schools.com/python/python_ref_keywords.asp" target="_blank">w3schools.org</a>.
- It is recommended to separate words with underscores and use lowercase names.

```python
var1 = 50
var2 = 100
var3 = var1 + var2
listvariables = [var1, var2, var3]
print(var1) # Output: 50
print(var2) # Output: 100
print(var3) # Output: 150
print(var1+var2+var3) # Output: 300
print(listvariables) # Output: [50, 100, 150]
```

## 3. if ... elif ... else ...

- This is a conditional code block, meaning that the code will run if the condition specified on the if statement is met.
- The elif statement is used if the if statement's condition is not met but the condition on the elif statement is met.
- The else statement is used after all conditions are not met.
- When comparing 2 numeric values, you must use the == sign (equal to), the >= sign (greater than or equal to), the <= sign (less than or equal to), the < (less than) sign, the > (greater than) sign, or the != sign (not equal to).
- Remember that the = sign assigns a value to a variable, and the == sign compares 2 values.
- To combine multiple conditions, you can use the operators and, or, not.
```python
number = 80
target = 100
if number == target:
  print("Congratulations!")
elif number < target:
  print("Unfortunately, you scored less than the target.")
else:
  print("Unfortunately, you scored more than the target.")
# Output: Unfortunately, you scored less than the target.
```

## 4. for i in ...

- This block of code performs an action or set of actions for a specified number of times.
- You can change the increment value of i to increase by multiple values.
- You can also use this loop to go through every item in a list.
- If you use the range statement, the default starting value is 0.

```python
for i in range(10):
  print(i)
# Output:
# 0
# 1
# 2
# 3
# 4
# 5
# 6
# 7
# 8
# 9
```

```python
for i in range(1, 10, 2): # First parameter (value) in the range statement is the start value, second parameter is the stop value, third parameter is the increment (the block ends if the current value of i exceeds the stop value
  print(i)
# Output:
# 1
# 3
# 5
# 7
# 9
```

```python
to_do_list = ["breakfast", "code", "lunch", "gym", "dinner"]
for activity in to_do_list:
  print(activity)
# Output:
# breakfast
# code
# lunch
# gym
# dinner
```

## 5. f"This is an f-string, using a variable of {var}."

- The f-string, also known as a formatted string literal, allows you to add variables with ease.
- Wrap the variable around curly brackets {} so you don't have to concatenate (combine) strings.

```python
points1 = 100
pointsgoal = 200
print(f"I scored {points1} points today. I have a goal of scoring {pointsgoal} points by the end of the day.") # Output: I scored 100 points today. I have a goal of scoring 200 points by the end of the day.
```

## 6. string[0:8], list[0:8]

- Substrings and sublists are used to split strings and lists.
- The index of a string or list is the position of a character or list item in order, beginning with index 0.
- The first parameter is the start index, and the second parameter is the first index to be excluded from the substring or sublist.
- You can omit the first parameter if you want to start at index 0 or omit the second parameter if you want to end at the same index as the original string or list.
- You can use negative values counting down; -1 represents the end of the string/list, -2 represents the character/item beforehand, and so on.
- To slice individual characters/items, use the index of the character/item.
- The indices included must be within the range of the string or list. For example, if I have a list containing 5 items, any value greater than index 4 (ending index) is out of range. The same goes with anything less than index -5 (starting negative index).

```python
birthday = "March 7, 1992" # Not my actual birthday
month = [:5]
day = [6]
year = [-4:]
activities = ["eat", "play", "code", "read"]
good_activities = activities[0:3]
print(f"On {month} {day}, {year}, I like to do the following activities:") # Output: On March 7, 1992, I like to do the following activities:
print(good_activities) # Output: ['eat', 'play', 'code']
```

## 7. def function() ...

- After the def keyword, the function can be named anything as long as it follows the variable naming rules/conventions.
- Functions let you create a custom code block that can be called any time.
- A function can contain optional arguments.
- Variables stored inside a function are called local variables; they are usually returned after all tasks are done, ending the function.
- Variables outside the function are called global variables; they can be used anywhere.
- Functions are useful for repeated code blocks.

```python
def add(a, b):
  sum = a + b
  return sum

def greeting():
  print("Hello")
  print("How are you?")

random = add(10, 5)
print(random) # Output: 15
greeting() 
# Output:
# Hello
# How are you?
```

## 8. input()

- You can set a variable to equal a user input value.
- The input is stored as a string, so you need to convert it to other data types if necessary.

```python
feeling = input("How are you feeling today?") # Input: good
print(f"I am feeling {feeling} today.") # Output: I am feeling good today.
```

## 9. len()

- Use the len function and put any variable with multiple indices to find the length of the object. This works for lists, strings, sets, tuples, dictionaries, etc.

```python
name = "Ethan"
items = ["apple", "orange", "banana"]
print(len(name)) # Output: 5
print(len(items)) # Output: 3
```

## 10. str(), int(), float(), bool()

- str() converts a Python object to a string.
- int() converts a Python object to an integer.
- float() converts a Python object to a float, or a number with a decimal value.
- bool() converts a Python object to a boolean value; a True/False value.

```python
print(str(9)) # Output: 9
print(int("50")) # Output: 50
print(float("29.1")) # Output: 29.1
print(bool("")) # Output: False
print(bool(10 > 5)) # Output: True
print(bool(8 < 8)) # Output: False
print(bool("Hello")) # Output: True
```

## Final Thoughts
Each of these Python statements/code blocks are essential for beginner Python programs, so put them to good use! With that being said, I hope you learned something useful today! Happy coding!
