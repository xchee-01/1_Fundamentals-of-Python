# 9. While loops

While loops are fundamental programming constructs that allow code to execute repeatedly as long as a specified condition remains true. They are particularly useful when working with data processing and iterative calculations in medical research.

## 9.1. Basic while loops

This is the syntax for a basic while loops

```
# Basic structure
while condition:
    # code block to execute
    # update condition
```

Here is a simple medical example

```
mutation_probability = 0.8
while mutation_probability > 0.2:
    # Simulate DNA repair mechanism
    mutation_probability *= 0.5
    print(f"Mutation probability after repair: {mutation_probability:.3f}")
```

> [!TIP]
> This statement here `f"Mutation probability after repair: {mutation_probability:.3f}"` is known as string formatting. String formatting is a way to insert values into predefined text patterns using placeholders.
>
> ```
> name = "Alice"
> age = 25
> message = f"My name is {name} and I'm {age} years old"  # Using f-strings
> ```
> 
> You can also use numbers for string formatting as well
>
> ```
> price = 1234.5678
> formatted_price = f"{price:.2f}"
> ```

## 9.2. Input validation and error handling

Input validation using while loops ensures data integrity, which is crucial when dealing with patient data or experimental results.

```
while True:   #This is needed to create an infinite loop that continues until valid input is received
    try:
        ph_value = float(input("Enter pH value (0-14): "))
        if 0 <= ph_value <= 14:
            print("This is a valid pH value")
            break
        else:
            print("pH must be between 0 and 14")
    except ValueError:
        print("Please enter a valid number")
```

## 9.3. Loop control and exit conditions

Similar to the while loop, it's good practice to put in loop control statements. Loop control statements help manage program flow and provide ways to exit loops based on specific conditions. This is essential when processing large datasets or running simulations.

```
# Break statement example
gene_sequence = "ATCGTTAA"
target = "TAA"
position = 0

while position < len(gene_sequence):
    if gene_sequence[position:position+3] == target:
        print(f"Stop codon found at position {position}")
        break
    position += 1
```

## 9.4. Menu-driven programmes and interactive systems

With loops, it is now possible for you to write a simple programme. Menu-driven programs are essential for laboratory information systems and data analysis platforms. They provide an intuitive interface for users to interact with complex computational tools.


```
while True:
    # Display menu
    print("\n1. Analyze DNA sequence")
    print("2. Calculate protein mass")
    print("3. Search mutation database")
    print("4. Exit")
    
    choice = input("Enter your choice (1-4): ")
    
    if choice == '1':
        print("DNA sequence analysis activated")
        pass
    elif choice == '2':
        print("Protein mass calculation activated")
        pass
    elif choice == '3':
        print("Searching for mutations in database")
        pass
    elif choice == '4':
        print("Exiting program")
        break
    else:
        print("Invalid choice, please try again")
```
