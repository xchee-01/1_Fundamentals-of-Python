# 5. Variables and operators

## 5.1. Variables 

### 5.1.1. What are variables?  

Variables are containers for storing data values. Python has specific conventions that help make code readable and maintainable.

Understanding how to properly name and manage variables is crucial for writing clean, maintainable code that other scientists and developers can easily understand.

**Rules and Best Practices:** 

- Start with a letter or underscore
- Can contain letters, numbers, and underscores
- Case-sensitive
- Use descriptive names that indicate purpose
- Follow snake_case convention for Python]

Here are examples of what constitutes good and bad naming. 

```
# Good naming
user_age = 25
total_score = 100
first_name = "John"

# Bad naming
a = 25
t = 100
fn = "John"
```

### 5.1.2. Variables can be assigned and re-assigned

Assignment gives a value to a variable, while reassignment changes that value. Python makes this process straightforward and flexible.

```
# Initial tumor size
tumor_diameter = 2.5  # in cm

# After treatment reassignment
tumor_diameter = 1.8  # in cm
```

### 5.1.3. Variables can be indicated as constants

Constants are variables whose values should not change throughout the program. In Python, they're typically indicated by uppercase names. _The value can still technically be changed (Python doesn't enforce true constants)._

```
NORMAL_BODY_TEMP = 37.0
MIN_BLOOD_OXYGEN = 95
PATHOGENIC_THRESHOLD = 0.90
```

> [!TIP]
> Best practice is to place constants at the module level (top of the file) so they're easily visible and maintainable.

### 5.1.4. Not all variables can be accessed all the time 

This is known as **variable scope**. Scope determines where in your code a variable can be accessed. There are primarily three types of scope in Python:

- Global variables can be accessed from anywhere in your code
- Local variables are only accessible within their defined function
- Nested functions can access variables from their parent function (enclosing scope)

```
# 1. Global Scope
global_variable = "I'm accessible everywhere"

def first_function():
    # 2. Local Scope (Function Scope)
    local_variable = "I'm only accessible inside this function"
    print(global_variable)  # Can access global variable
    print(local_variable)   # Can access local variable
    
    def nested_function():
        # 3. Enclosing (Nonlocal) Scope
        nested_variable = "I'm only accessible in this nested function"
        print(local_variable)    # Can access parent function's variables
        print(nested_variable)   # Can access its own variables
```

You can try this out

```
print(global_variable)  # Would raise an error
print(local_variable)  # Would raise an error
print(nested_variable)  # Would raise an error
```

## 5.2. Operators

Operators are special symbols that perform operations on variables and values.

### 5.2.1. Arithmetic operators

```
x = 10
y = 3

addition = x + y        # 13
subtraction = x - y     # 7
multiplication = x * y  # 30
division = x / y        # 3.333...
modulus = x % y        # 1
exponent = x ** y      # 1000
```

### 5.2.2. Comparison operators

```
x = 5
y = 10

equal = x == y          # False
not_equal = x != y      # True
greater = x > y         # False
less = x < y            # True
greater_equal = x >= y  # False
less_equal = x <= y     # True
```

### 5.2.3. Logical operators

```
x = True
y = False

and_result = x and y  # False
or_result = x or y    # True
not_result = not x    # False
```

### 5.2.4. Assignment operators

```
x = 5
x += 3   # x = x + 3 (8)
x -= 2   # x = x - 2 (6)
x *= 2   # x = x * 2 (12)
x /= 3   # x = x / 3 (4)
```

> [!NOTE]
> Determines the order in which different operators are evaluated in an expression.
> Order (highest to lowest):
> 
> 1. Parentheses ()
> 2. Exponentiation **
> 3. Multiplication/Division/Modulus *, /, %
> 4. Addition/Subtraction +, -
> 5. Comparison operators <, >, <=, >=, ==, !=
> 6. Logical operators not, and, or
>
> For example,
>
> ```
> result = 2 + 3 * 4    # 14 (not 20)
> result = (2 + 3) * 4  # 20
> ``` 
