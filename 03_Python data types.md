# 3 Python data types

## 3.1 Numbers (integers and floating-point)

It is important to understand numerical data types is crucial as they form the foundation for scientific calculations and quantitative analyses. 

Python has two types of numbers, namely, integers and floating points. 

**(a) Integers**

Integers are whole numbers without decimal points (like -3, 0, 42).

```
# Basic integers
patient_id = 12345
chromosome_number = 23

# Real-world example: Genomic Position
start_position = 234567890  # Starting position of a gene on chromosome
```

**(b) Floating points**

Floating point numbers can represent decimal values (like 3.14, -0.5, 2.0).

```
# Basic floats
temperature = 37.5
pH_level = 7.4

# Real-world example: Gene Expression Values
expression_level = 2.45  # Log2 fold change in gene expression
p_value = 1.23e-10      # Statistical significance of expression
```

## 3.2 Strings and strings operations

Strings are essential for handling sequence data, patient information, and biological identifiers.

```
# Basic string operations
name = "BRCA1"
sequence = "ATGCTAGCT"
```

There are some methods that you can apply onto strings. 

```
# String methods
print(sequence.count('A'))  # Count adenine occurrences
print(sequence[:3])        # Get first three nucleotides

# Real-world example: DNA Sequence Processing
dna_sequence = "ATGCTAGCTGACTACGT"
complement = dna_sequence.replace('A','T').replace('G','C').replace('C','G').replace('T','A')
print(f"Original: {dna_sequence}")
print(f"Complement: {complement}")
```

> [!NOTE]
> A Python method is a function that belongs to a class and operates on class instances (objects)
> So, a `count()` is a **method** that belongs to Pythons string **class**.
> In this case, the method is being applied to an **object**

## 3.3 Booleans

Boolean values are crucial for conditional operations and filtering biological data.

```
# Basic booleans
is_coding = True
is_pathogenic = False

# Real-world example: Variant Classification
def is_clinically_significant(variant_score):
    return variant_score > 0.8 and variant_score < 1.0

variant_pathogenic = is_clinically_significant(0.95)
```

> [!CAUTION]
> It is very important for you to know what kind of data type that you are working on.
> You can check this by using the `type()` method.
>
> ```
> string_value = '37.5' #This seems like a floating point
> type(string_value) #This would return str
> ```
>
> Hence you would need to convert this into floating point using **type conversion**
>
> ```
> numeric_value = float(string_value)
> type(numerica_value)
> ```
> 
> Here's a real world example
> 
> ```
> #Real-world example: Processing Clinical Data
> patient_data = "1234,BRCA1,0.89"
> id, gene, score = patient_data.split(',')
> processed_score = float(score)
> is_significant = processed_score > 0.85
> ```


