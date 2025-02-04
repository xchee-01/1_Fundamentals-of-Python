# 8. For loops

## 8.1. Basics of for loops

For loops are important building blocks of iteration. 
The basic syntax of for loops are as follows:

```
for variable in sequence:
    # code block to be repeated
```

Here are some simple example:

```
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

```
amino_acids = ["Glycine", "Alanine", "Valine"]
for acid in amino_acids:
    print(f"Processing amino acid: {acid}")
```

## 8.2. Combining the use of for loops with range

The `range()` function generates a sequence of numbers that is perfect for controlled iterations 

> [!NOTE]
> The syntax of the `range()` function is as follows:
> range(stop)           # 0 to stop-1
> range(start, stop)    # start to stop-1
> range(start, stop, step)  # start to stop-1 with step interval

Here's a simple example of how for loops can be used together with range()

```
for i in range(3):
    print(f"Iteration {i}")
```

## 8.3. Loop control statements 

Loop control statements like break, continue, and return are essential because they give you precise control over program flow, letting you exit loops early, skip iterations, or handle specific conditions - making your code more efficient and preventing infinite loops.

> [!CAUTION]
> You can try this out if you are keen but this will go into an infinity loop, which is what you do not want to happen with your codes.
>
> ```
> for i in range(1):  # Even though range is 1, the loop never ends
>    print("This will print forever")
>    i = 0  # Resetting i keeps the loop going
> ```

**(a) Break statement:**

A break statement allows the code to exit the loop completely. 

```
for i in range(5):
    if i == 3:
        break
    print(i)
```

**(b) Continue statement:***

A continue statement skips and continues on with the rest of the iteration

```
for i in range(5):
    if i == 3:
        continue
    print(i)
```

## 8.4. Nested loops

Nested loops are _loops within loops_ for handling multi-dimensional data structures. 

Here is a simple example

```
for i in range(2):
    for j in range(2):
        print(f"Position: {i},{j}")
```

and how you can apply this in a medical setting

```
patients = ["P1", "P2"]
biomarkers = ["TNF", "IL6", "CRP"]

for patient in patients:
    for marker in biomarkers:
        print(f"Analyzing {marker} levels in patient {patient}")
```

## 8.5. Enumeration

The enumerate() function in Python creates an iterator that returns pairs of (index, item) for each item in a sequence, making it easy to loop through items while keeping track of their position - for example, for i, item in enumerate(my_list) gives you both the index and value in each iteration.

Here is how you can do this:

```
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
    print(f"Index {index}: {fruit}")
```

## 8.6. List comprehension

A list comprehension is a concise way to create a new list by applying an expression to each item in an existing sequence (like a list, tuple, or string) and optionally filtering elements using a condition - it's basically a compact `for` loop packed into a single line.

Here is a simple example

```
numbers = [1, 2, 3, 4, 5]
squares = [num**2 for num in numbers]
```

> [!TIP]
> It is also possible to use loops to create visual patterns for data visualization!
> For example
>
> ```
> for i in range(5):
>   print('*' * i)
> ```
>
> or
>
> ```
> # Visualizing gene expression levels
> expression_levels = [2, 4, 1, 5]
> for level in expression_levels:
>     print('█' * level + f" ({level}x)")
> ```
