# 10. Python functions

Functions are fundamental building blocks in Python programming that allow us to encapsulate reusable code into organized, logical units. This lecture covers the essential concepts of function creation, usage, and advanced parameter handling.

## 10.1. Function definition and basic structure

Functions in Python are defined using the `def` keyword, followed by the function name and parentheses. A function can contain any number of statements and can be called multiple times throughout your code.

The basic syntax of a function is as follows:

```
def function_name():
    # Function body
    statements
```

Here is a simple example of illustrate how a custom function can be set up

```
def greet_user():
    print("Hello! Welcome to our program.")

# Calling the function
greet_user()  # Output: Hello! Welcome to our program.
```

## 10.2. Parameter and arguments

Parameters are variables listed in the function definition, while arguments are the values passed to the function when it's called. They allow functions to work with different inputs each time they're called.

The basic syntax of a function that takes in arguments is as follows:

```
def function_name(argument1, argument2):
    # Function body using arguments
    statements
```

For example,

```
def calculate_sum(a, b):
    total = a + b
    print(f"The sum of {a} and {b} is {total}")

# Calling with arguments
calculate_sum(5, 3)  # Output: The sum of 5 and 3 is 8
```

## 10.3. Default parameters and keyword arguments

Default parameters provide default values for parameters if no argument is provided. Keyword arguments allow you to specify arguments by parameter name.

The basic syntax is as follows:

```
def function_name(param1, param2=default_value):
    statements
```

For example,

```
def greet(name, greeting="Hello"):
    print(f"{greeting}, {name}!")

greet("Alice")  # Output: Hello, Alice!
greet("Bob", greeting="Hi")  # Output: Hi, Bob!
```

## 10.4. Variable length arguments

Python allows functions to accept a variable number of arguments using `*args` (for positional arguments) and `**kwargs` (for keyword arguments).

First, let's understand what these special arguments mean:

```
# *args allows you to pass any number of positional arguments
def sum_numbers(*args):
    total = 0
    for number in args:
        total += number
    return total

# You can call it with any number of arguments
print(sum_numbers(1, 2))          # Output: 3
print(sum_numbers(1, 2, 3, 4))    # Output: 10
```

Now let's look at **kwargs (keyword arguments):

```
# **kwargs allows you to pass any number of keyword arguments
def print_patient_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

# Call it with different keyword arguments
print_patient_info(name="John", age=30)
print_patient_info(name="Sarah", age=25, blood_type="A+", weight=65)
```

> [!NOTE]
> `*args` collects all positional arguments into a tuple
> `**kwargs` collects all keyword arguments into a dictionary
>
> When you used `**kwargs`:
>
> ```
> def person_details(**kwargs):
>     print(type(kwargs))  # This will show it's a dictionary
>     for key, value in kwargs.items():
>         print(f"{key}: {value}")
> 
> #When you call the function:
> person_details(name="John", age=25, city="New York")
> #This creates a dictionary: {"name": "John", "age": 25, "city": "New York"}
> ```


## 10.5. Return values

The `return` statement allows functions to send results back to the caller. Functions can return single values, multiple values, or nothing (returning None by default).

```
def multiply(x, y):
    result = x * y
    return result

product = multiply(4, 5)
print(product)  
```

> [!CAUTION]
> With `return`: The value can be stored in a variable and used later
> Without `return`: The function just performs an action but does not give back a value that you can use later in your code
>
> #Function WITHOUT return
> def multiply(x, y):
>     result = x * y
>
> product = multiply_no_return(4, 5) 
> print(product)  # Output: None  (because function didn't return anything)

> [!CAUTION]
> Variable scope also applies here. Make sure that your function can access all the variables that it needs

## 10.6. Lambda functions

Lambda functions are small, anonymous functions that can have any number of arguments but can only have one expression. They are useful for short operations that don't require a full function definition.

The basic syntax is as follows:

```
lambda arguments: expression
```

Here is a simple example:

```
square = lambda x: x**2
print(square(5))  # Output: 25
```

and another that is contextualized to the medical field 

```
calculate_bmi = lambda weight, height: weight / (height**2)
patient_bmi = calculate_bmi(70, 1.75)
print(f"Patient BMI: {patient_bmi:.2f}")
```

> [!CAUTION]
> Remember that lambda functions should be used sparingly and mainly for simple operations. For complex operations, regular functions are more appropriate and provide better readability and maintainability.

