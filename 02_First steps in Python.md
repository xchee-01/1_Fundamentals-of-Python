# 2 First steps in Python 

## 2.1 Writing your first program

We will do a classic "Hello, World!"

```
# Simple Hello World
print("Hello, World!")
```

Here is how you can apply it in a biomedical example

```
# Simple patient greeting system
patient_name = "John Doe"
diagnosis = "Type 2 Diabetes"
print(f"Welcome {patient_name}")
print(f"Your precision medicine profile for {diagnosis} is being analyzed")
```

## 2.2 Basic code structure and syntax

### 2.2.1 Python Syntax rules 

**(a) Indentation**

Python uses whitespace indentation (typically 4 spaces) to define code blocks and hierarchical structure, making it a fundamental part of the language's syntax rather than using braces or keywords.

```
if True:
    print("Indented with 4 spaces")
    print("Same block")
print("Different block")
```

**(b) Case Sensitivity**

Python is case-sensitive, meaning that identifiers like variables, function names, and classes with the same spelling but different capitalization (e.g., 'name', 'Name', and 'NAME') are treated as distinct entities.

```
gene = "BRCA1"
Gene = "BRCA2"
# gene and Gene are different variables
```

**(c) Line Continuation**

Python code lines can be continued across multiple lines using a backslash () character or implicit continuation within parentheses, brackets, or braces, making long statements more readable.

### 2.2.2 Variables and Data Types 

**(a) integer (int)**

Numbers without decimal points, used for counting and whole number calculations (e.g., 5, -17, 1000)

**(b) float**

Numbers with decimal points, used for precise calculations and measurements (e.g., 3.14, -0.001, 2.0)

**(c) string (str)**

A sequence of characters (letters, numbers, symbols) enclosed in quotes, used for text (e.g., "Hello World", 'Python')

**(d) boolean (bool)**

A data type with only two possible values - True or False, used for logical conditions and control flow

```
# Basic data types
patient_id = 12345                # integer
mutation_probability = 0.15       # float
patient_name = "Alice Smith"      # string
is_carrier = True                # boolean
```

## 2.3 Comments and documentation

**(a) Single line comments** 

Comments that begin with a '#' symbol and explain code in a brief, inline format, helping developers understand specific lines or small blocks of code.

```
# This is a single-line comment
patient_age = 45  # Patient's age in years
```


**(b) Multi-line comments (Docstrings)**

Multi-line string literals enclosed in triple quotes (''' or """) that serve as built-in documentation for Python modules, classes, methods, and functions, which can be accessed programmatically.

```
def analyze_mutation(gene_sequence):
    """
    Analyzes a given gene sequence for known pathogenic mutations.
    
    Parameters:
        gene_sequence (str): The DNA sequence to analyze
    
    Returns:
        bool: True if pathogenic mutation found, False otherwise
    """
    return True  # Placeholder return
```

**(c) Documentation best practices** 

There are a set of standardized guidelines that emphasize writing clear, concise, and consistent documentation that describes what the code does, its parameters, return values, and usage examples, following PEP 257 conventions. This will help others, as well as yourself, the next time you need to return to use the codes. 

**i. File headers:** 

```
"""
Gene Analysis Module
Author: Dr. Smith
Date: 2025-02-03
Purpose: Analyzes gene sequences for known pathogenic variants
"""

# Rest of the code follows
```

**ii. Function documentation:**

```
def calculate_drug_dosage(patient_weight, genetic_factor):
    """
    Calculates personalized drug dosage based on patient weight
    and genetic metabolism factors.
    
    Args:
        patient_weight (float): Weight in kg
        genetic_factor (float): Metabolism factor from 0.5 to 1.5
    
    Returns:
        float: Recommended drug dosage in mg
    """
    base_dose = 50  # mg
    return base_dose * (patient_weight/70) * genetic_factor
```
