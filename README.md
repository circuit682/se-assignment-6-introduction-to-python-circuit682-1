# Python Basics:

Python is a high-level, interpreted, general-purpose programming language. It was created by Guido van
Rossum in 1991 and has become one of the most popular programming languages in the world.
Python is known for its readability, simplicity, and versatility. It is often used for web development,
data analysis, scientific computing, and machine learning. It is also widely used in academia and
industry for teaching and research purposes.

Python is an object-oriented programming language, which means that it allows developers to create
objects that can be used to represent real-world entities. These objects can have attributes and
methods, which can be used to manipulate the object's state and behavior. Python also supports
functional programming, which allows developers to write code in a more declarative style.
Python is also known for its dynamic typing, which means that variables can be assigned values of
different types at runtime. This makes it easier to write code that is flexible and adaptable to
changing requirements.

# Examples of use cases where Python is particularly effective.

1. Data Analysis and Visualization
Use Case: Analyzing large datasets to extract meaningful insights.

2. Web Development
Use Case: Developing web applications and RESTful APIs.

3. Machine Learning and AI
Use Case: Building and deploying machine learning models.

# Installing Python on MAC:
# Step 1: Install Homebrew
This is a package manager for macOS that makes it easy to install software. 

# Step 2: Install Python 3
Run the following command:

********brew install python3

# Step 3: Verifying the Installation
python3 --version
pip3 --version
# Step 4: Setting up a Virtual Environment
A virtual environment is a self-contained directory tree that contains a Python installation for a
particular version of Python, plus a number of additional packages. This allows you to work on
multiple projects at the same time without having to worry about conflicts between different
versions of Python or packages.
To create a virtual environment, run the following command:
********python3 -m venv myenv
This will create a directory called myenv in the current directory. To activate the virtual
environment, run the following command:
********source myenv/bin/activate

# Data Types and Variables in PYTHON:
1. Integers (int):Whole numbers, positive or negative, without a decimal point.
2. Floating-Point Numbers (float):Numbers with a decimal point.
3. Strings (str):Text enclosed in quotes.
4. Booleans (bool):True or False values.
5. Lists (list):Ordered collections of values.
6. Tuples (tuple):Ordered collections of values that cannot be modified.
7. Dictionaries (dict):Unordered collections of key-value pairs.
8. Sets (set):Unordered collections of unique values.

# A Script Demonstrating Different Data Types:

```
# Integer
x = 42
print("Integer:", x)

# Float
y = 3.14
print("Float:", y)

# String
z = "Hello, world!"
print("String:", z)

# Boolean
is_valid = True
print("Boolean:", is_valid)

# List
fruits = ["apple", "banana", "cherry"]
print("List:", fruits)

# Tuple
coordinates = (10.0, 20.0)
print("Tuple:", coordinates)

# Dictionary
person = {"name": "Alice", "age": 25}
print("Dictionary:", person)

# Set
unique_numbers = {1, 2, 3, 4, 4, 5}
print("Set:", unique_numbers)
```

# Control Structures:
Conditional statements in Python allow one to execute certain pieces of code based on specific conditions.

******Examples of an `if-else` statement:
# Define a variable
temperature = 25

# Use an if-else statement to check the temperature
```
if temperature > 30:
    print("It's a hot day!")
elif temperature > 20:
    print("It's a nice day!")
else:
    print("It's a bit cold today!")
```

# The use of  loops in Python:
Loops are used to repeat a block of code multiple times. The most common types of loops are for and while loops.

*****Example of a for Loop:
```
#Define a list of fruits
fruits = ["apple", "banana", "cherry"]

#Use a for loop to iterate over the list of fruits
for fruit in fruits:
    print(fruit)
```

#  Functions in Python:
Functions in Python are blocks of organized, reusable code that perform a specific task.

******Why funtions are useful:
They enable for; modularity, flexibility, readability of code, it's maintainability and enabled encapsulation.

*******A Python Function Example:
```
#Define the function
def add_numbers(a, b):
    """Returns the sum of a and b."""
    return a + b

#Call the function with two numbers
result = add_numbers(5, 3)

#Print the result
print("The sum is:", result)
```

# Differences Between Lists and Dictionaries in Python:

****** Difference in Structure:
Lists: Ordered collections of items that are indexed by integers starting from 0.
Dictionaries: Unordered collections of key-value pairs, where each key is unique.

****** Difference in Access:
Lists: Access items by their index.
Dictionaries: Access items by their keys.

****** Difference in Use Cases:
Lists: Useful for storing ordered sequences of items, such as a collection of numbers, strings, or objects.
Dictionaries: Useful for storing associative arrays or mappings, such as a set of key-value pairs where you need to look up values based on custom keys.

******Sample script:

# Creating a list of numbers and performing operations
```
numbers = [10, 20, 30, 40, 50]
print("Original List:", numbers)

# Basic operations on the list
# Append a number to the list
numbers.append(60)
print("After Append:", numbers)

# Insert a number at a specific position
numbers.insert(2, 25)
print("After Insert:", numbers)

# Remove a number from the list
numbers.remove(30)
print("After Remove:", numbers)
```

# Creating a dictionary with key-value pairs and performing operations
```
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}
print("Original Dictionary:", person)

# Basic operations on the dictionary
# Add a new key-value pair
person["email"] = "alice@example.com"
print("After Adding Email:", person)
```

# Exception Handling in Python
Exception handling in Python is a way to handle errors gracefully, allowing the program to continue running or to fail in a controlled manner.

*******An example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script:
```
def divide_numbers(a, b):
    try:
        result = a / b
    except ZeroDivisionError as e:
        print("Error: Cannot divide by zero!")
        result = None
    except TypeError as e:
        print("Error: Invalid input types!")
        result = None
    else:
        print("Division successful!")
    finally:
        print("Execution completed.")
    return result

# Create a list of numbers and a dictionary
numbers = [10, 20, 0, 'a']
results = {}

# Iterate over the list and perform division
for number in numbers:
    result = divide_numbers(100, number)
    results[number] = result

print("Results:", results)
```

# Modules and Packages in Python:
Modules
A module in Python is a file containing Python code (definitions, functions, variables, classes, etc.) that you can include in your program.
Packages
A package is a collection of modules organized in directories that provide a hierarchy of module names.

******How to import and use a module in a script:
To use a module in a script, one must import it using the import statement. 
Here's how you can do it with the math module, which is a standard module in Python providing mathematical functions.

`import math`

*****A sample snippent:

```import math

# Using sqrt() function to calculate the square root
num = 16
sqrt_value = math.sqrt(num)
print(f"The square root of {num} is {sqrt_value}")

# Using pi constant
radius = 5
area = math.pi * (radius ** 2)
print(f"The area of a circle with radius {radius} is {area}")

# Using sin() function to calculate the sine of an angle (in radians)
angle = math.radians(30)  # Convert 30 degrees to radians
sine_value = math.sin(angle)
print(f"The sine of 30 degrees is {sine_value}")
```

# How to read from and write to files in Python:
*****
To read the content of a file, you can use the following steps:

1. Open the file using open() in read mode ('r').
2. Read the content using read() method.
3. Close the file using close() method.

```
# Open the file in read mode
with open('example.txt', 'r') as file:
    # Read the content of the file
    content = file.read()

# Print the content
print(content)
```

# Writing to a File
To write a list of strings to a file, you can use the following steps:

1. Open the file using open() in write mode ('w').
2. Write the content using write() method.
3. Close the file using close() method.

```
# List of strings to write to the file
lines = [
    "First line of text\n",
    "Second line of text\n",
    "Third line of text\n"
]

# Open the file in write mode
with open('output.txt', 'w') as file:
    # Write each line to the file
    file.writelines(lines)
```




























