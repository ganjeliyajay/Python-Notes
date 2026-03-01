# Intermediate Python Notes (Simple + Detailed)

These notes explain Python concepts in **very simple English with examples** so beginners can understand easily.

---

# 1. Evolution of Python

Python is a **high‑level programming language** created to make programming simple and readable.

### What High-Level Means

A high‑level language is closer to human language and easier to understand compared to low‑level languages like C.

Example:

```python
print("Hello World")
```

This single line prints text on the screen.

### History

* Python was created by **Guido van Rossum**
* Development started in **1989**
* First release was **Python 1.0 in 1991**
* Name inspired by the comedy show **Monty Python**

### Why Python Was Created

Python was designed to:

* Make programming easy
* Reduce complicated syntax
* Allow developers to write fewer lines of code
* Improve readability

Example comparison:

C Language:

```c
#include <stdio.h>
int main(){
 printf("Hello World");
}
```

Python:

```python
print("Hello World")
```

Python requires far less code.

---

# 2. Major Versions of Python

## Python 1.0

Released in **1991**.

Features:

* Functions
* Modules
* Exception handling
* Basic data structures like lists and dictionaries

## Python 2.0

Released in **2000**.

Features:

* List comprehensions
* Garbage collection
* Better memory management

Python 2 support officially ended in **2020**.

## Python 3.0

Released in **2008**.

Major improvements:

* Better Unicode support
* Cleaner syntax
* Better division behavior

Example:

```python
5/2
```

Output in Python 3:

```
2.5
```

## Modern Python (3.x)

Recent features include:

* f-strings
* async programming
* type hints

Example:

```python
name = "Jay"
print(f"Hello {name}")
```

---

# 3. Role of Python in Modern Computing

Python is used in many fields.

## Web Development

Python is used to build websites and APIs.

Popular frameworks:

* Django
* Flask

Example:

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
 return "Hello World"
```

## Data Science

Python is heavily used for data analysis.

Popular libraries:

* NumPy
* Pandas
* Matplotlib

Example:

```python
import pandas as pd

data = {"Name":["A","B"],"Marks":[80,90]}

df = pd.DataFrame(data)

print(df)
```

## Artificial Intelligence

Python is widely used in AI and Machine Learning.

Libraries:

* TensorFlow
* PyTorch
* Scikit‑learn

Applications:

* Chatbots
* Image recognition
* Recommendation systems

## Automation

Python can automate repetitive tasks.

Example:

```python
import os

files = os.listdir()
print(files)
```

---

# 4. Python Installation

Steps:

1. Go to python.org
2. Download Python
3. Run installer
4. Select **Add Python to PATH**
5. Click install

Verify installation:

```bash
python --version
```

---

# 5. Python IDEs

IDE means **Integrated Development Environment**.

It is software used to write and run programs.

## IDLE

Default Python editor.

Best for beginners.

## Jupyter Notebook

Used mainly in **data science**.

Features:

* Run code in cells
* Supports charts
* Allows documentation

## Anaconda

Python distribution for scientific computing.

Includes:

* many libraries
* Jupyter Notebook
* conda package manager

---

# 6. Python Memory Model

Python stores everything as **objects in memory**.

Variables store **references to objects**.

Example:

```python
a = 10
b = a
```

Both variables point to the same value.

## Garbage Collection

Python automatically removes unused objects from memory.

Benefits:

* saves memory
* avoids memory leaks

---

# 7. Variables

A variable is a name used to store data.

Example:

```python
age = 20
name = "Jay"
```

Rules for variables:

* must start with letter or underscore
* cannot start with number
* cannot use keywords
* case sensitive

Valid examples:

```python
score = 90
_score = 50
```

---

# 8. Constants

Constants are values that should not change.

Python does not enforce constants but programmers use **uppercase naming convention**.

Example:

```python
PI = 3.14159
MAX_USERS = 100
```

---

# 9. Expressions

An expression is a combination of values, variables, and operators.

Example:

```python
a = 5
b = 10

result = a + b
```

Types of expressions:

* arithmetic
* logical
* comparison

---
# 10. Data Types

In Python, **data types** define the type of value a variable can store. Every value in Python belongs to a specific data type. Understanding data types helps us know **what kind of operations we can perform on a value**.

Python automatically detects the data type when a variable is assigned. This makes Python very easy for beginners.

Example:

```python
x = 10
```

Python automatically understands that **10 is an integer**.

---

## Integer (int)

Integers are **whole numbers without decimal points**.

They can be:

* positive numbers
* negative numbers
* zero

Examples:

```python
x = 10
age = 25
score = -5
```

Common operations with integers:

```python
a = 10
b = 5

print(a + b)  # addition
print(a - b)  # subtraction
print(a * b)  # multiplication
```

Output:

```
15
5
50
```

---

## Float (float)

Float numbers are **numbers with decimal points**.

These are commonly used for:

* scientific calculations
* measurements
* percentages

Examples:

```python
y = 10.5
price = 99.99
percentage = 87.5
```

Example calculation:

```python
length = 5.5
width = 2.5

area = length * width

print(area)
```

Output:

```
13.75
```

---

## Complex Numbers (complex)

Complex numbers contain **two parts**:

* real part
* imaginary part

The imaginary part uses **j** in Python.

Example:

```python
z = 2 + 3j
```

Here:

* 2 = real part
* 3j = imaginary part

Example:

```python
x = 1 + 2j
y = 3 + 4j

print(x + y)
```

Output:

```
(4+6j)
```

Complex numbers are mostly used in **advanced mathematics and engineering**.

---

## String (str)

Strings are used to **store text data**.

Strings can be written using:

* single quotes
* double quotes

Examples:

```python
name = "Python"
city = 'Surat'
message = "Hello World"
```

Strings support many operations.

Example:

```python
name = "Jay"

print("Hello " + name)
```

Output:

```
Hello Jay
```

Example: string length

```python
text = "Python"

print(len(text))
```

Output:

```
6
```

---

## Boolean (bool)

Boolean values represent **True or False**.

They are mainly used in **conditions and decision making**.

Example:

```python
is_student = True
```

Example with condition:

```python
age = 18

print(age >= 18)
```

Output:

```
True
```

---

# 11. Operators 

Operators are **symbols used to perform operations on variables and values**.

Example:

```python
x = 10
y = 5

print(x + y)
```

Here **+** is an operator.

Python provides several types of operators.

---

## Arithmetic Operators

Used for mathematical calculations.

```
+   Addition
-   Subtraction
*   Multiplication
/   Division
%   Modulus (remainder)
**  Exponent (power)
```

Example:

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.33
print(a % b)   # 1
print(a ** b)  # 1000
```

---

## Comparison Operators

These operators compare two values and return **True or False**.

```
==   Equal
!=   Not Equal
>    Greater than
<    Less than
>=   Greater or equal
<=   Less or equal
```

Example:

```python
x = 10

y = 5

print(x > y)
print(x == y)
print(x != y)
```

Output:

```
True
False
True
```

---

## Logical Operators

Logical operators combine multiple conditions.

```
and
or
not
```

### and

Both conditions must be true.

```python
x = 10

print(x > 5 and x < 20)
```

Output:

```
True
```

### or

At least one condition must be true.

```python
print(5 > 10 or 10 > 5)
```

Output:

```
True
```

### not

Reverses the condition.

```python
print(not True)
```

Output:

```
False
```

---

# 12. Dynamic Typing

Python uses **dynamic typing**.

This means we **do not need to declare the data type of a variable**.

Python automatically decides the type during runtime.

Example:

```python
x = 10
print(type(x))
```

Output:

```
<class 'int'>
```

Now change the value.

```python
x = "Hello"
print(type(x))
```

Output:

```
<class 'str'>
```

This shows that **the same variable can store different types of data**.

---

# 13. Type Casting

Type casting means **converting one data type into another data type**.

Python provides built‑in functions for conversion.

Common functions:

```
int()
float()
str()
bool()
```

Example:

```python
x = "100"

y = int(x)

print(y + 50)
```

Output:

```
150
```

Convert integer to string:

```python
num = 10
text = str(num)

print("Number is " + text)
```

Convert float:

```python
x = 10

print(float(x))
```

Output:

```
10.0
```

---

# 14. Input and Output

Programs often need to **take input from users and display results**.

---

## Input

The **input() function** is used to take input from the user.

Example:

```python
name = input("Enter your name: ")
```

If the user types:

```
Jay
```

Then the variable **name** will store "Jay".

Important: input always returns **string data**.

Example:

```python
age = int(input("Enter age: "))
```

---

## Output

The **print() function** is used to display output.

Example:

```python
print("Hello", name)
```

Output:

```
Hello Jay
```

Multiple values can also be printed.

```python
name = "Jay"
age = 20

print(name, age)
```

---

# 15. Python Modes

Python programs can run in two main modes.

---

## Interactive Mode

Interactive mode allows us to **run Python commands one by one**.

It is useful for:

* quick testing
* learning Python
* trying small code snippets

Example:

```
>>> 2 + 2
4
```

Python executes the command immediately.

---

## Script Mode

Script mode is used for **writing complete programs in files**.

Python files use the extension:

```
.py
```

Example file:

```
program.py
```

Example code inside file:

```python
print("Hello Python")
```

Run the program using terminal:

```bash
python program.py
```

Output:

```
Hello Python
```

---

## Advantages of Script Mode

* suitable for large programs
* easier debugging
* better code organization
* easier maintenance

Script mode is commonly used for **real-world applications**.


# 16. Virtual Environments

Virtual environment is an isolated environment for Python projects.

Benefits:

* avoid library conflicts
* manage dependencies

Create environment:

```bash
python -m venv myenv
```

Activate:

```bash
myenv\\Scripts\\activate
```

---

# 17. Package Management

## pip

Install package:

```bash
pip install numpy
```

Remove package:

```bash
pip uninstall numpy
```

## conda

Example:

```bash
conda install pandas
```

---
# 18. Conditional Statements

Conditional statements allow a program to **make decisions** based on conditions.

Real-life example:

* If it rains → take an umbrella
* Otherwise → do not take an umbrella

Programming follows the same idea.

---

## if Statement

The **if statement** executes a block of code only when the condition is true.

```python
x = 10

if x > 5:
    print("x is greater than 5")
```

Explanation:

Python checks the condition `x > 5`. If the condition is true, the code inside the block runs.

---

## if else Statement

Used when there are **two possible outcomes**.

```python
age = 18

if age >= 18:
    print("You can vote")
else:
    print("You cannot vote")
```

Explanation:

* If the condition is true → first block runs
* If false → else block runs

---

## if elif else Statement

Used when **multiple conditions** must be checked.

```python
marks = 75

if marks >= 90:
    print("Grade A")
elif marks >= 70:
    print("Grade B")
elif marks >= 50:
    print("Grade C")
else:
    print("Fail")
```

Python checks conditions **from top to bottom**.

---

## Nested if

A nested if means an **if statement inside another if**.

```python
num = 10

if num > 0:
    if num % 2 == 0:
        print("Positive Even Number")
```

---

## Ternary Operator

A short one-line version of if-else.

```python
age = 20

result = "Adult" if age >= 18 else "Minor"

print(result)
```

---

# 19. Loops (Iteration)

Loops allow us to **repeat a block of code multiple times**.

Python mainly provides two types of loops:

* for loop
* while loop

---

## for Loop

The **for loop** is used to iterate over sequences like lists, strings, or ranges.

```python
for i in range(5):
    print(i)
```

Output

```
0
1
2
3
4
```

Example with list:

```python
fruits = ["apple", "banana", "mango"]

for fruit in fruits:
    print(fruit)
```

---

## while Loop

The **while loop** runs as long as the condition is true.

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

Important: Always update the variable inside the loop to avoid **infinite loops**.

---

## Nested Loops

A loop inside another loop.

```python
for i in range(3):
    for j in range(2):
        print(i, j)
```

Nested loops are often used for **matrix operations or pattern printing**.

---

# 20. Loop Control Statements

Loop control statements change the normal execution of loops.

Python provides:

* break
* continue

---

## break Statement

The **break statement stops the loop immediately**.

```python
for i in range(10):

    if i == 5:
        break

    print(i)
```

Output

```
0
1
2
3
4
```

---

## continue Statement

The **continue statement skips the current iteration** and moves to the next iteration.

```python
for i in range(5):

    if i == 2:
        continue

    print(i)
```

Output

```
0
1
3
4
```

---

# 21. Loop Else

Python allows an **else block with loops**.

The else block runs when the loop finishes normally.

```python
for i in range(3):
    print(i)
else:
    print("Loop completed")
```

If the loop stops using `break`, the else block will not run.

---

# 22. Functional Programming in Python

Functional programming is a programming style that focuses on **using functions to process data**.

Important tools include:

* Recursion
* Lambda functions
* map()
* filter()
* reduce()

These tools help write **short and powerful code**.

---

# 23. Recursion

Recursion is a technique where a **function calls itself**.

A recursive function must have:

1. Base case (stopping condition)
2. Recursive case (function calling itself)

Example: factorial

```python
def factorial(n):

    if n == 1:
        return 1

    return n * factorial(n-1)

print(factorial(5))
```

Output

```
120
```

---

# 24. Lambda Functions

A **lambda function** is a small anonymous function.

Syntax

```python
lambda arguments : expression
```

Example

```python
square = lambda x: x * x

print(square(5))
```

Output

```
25
```

---

# 25. map() Function

The **map() function applies a function to each element of an iterable**.

```python
numbers = [1,2,3,4]

result = list(map(lambda x: x*2, numbers))

print(result)
```

Output

```
[2,4,6,8]
```

---

# 26. filter() Function

The **filter() function selects elements from an iterable based on a condition**.

```python
numbers = [1,2,3,4,5]

result = list(filter(lambda x: x%2==0, numbers))

print(result)
```

Output

```
[2,4]
```

---

# 27. reduce() Function

The **reduce() function performs cumulative computation on elements**.

```python
from functools import reduce

numbers = [1,2,3,4]

result = reduce(lambda x,y: x+y, numbers)

print(result)
```

Output

```
10
```
