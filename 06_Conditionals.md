# 6. Conditionals

Conditional statements are the backbone of decision-making in programming. They allow your code to take different paths based on whether certain conditions are true or false – much like how different treatment paths might be chosen based on a patient's genetic markers.

## 6.1. Boolean expressons

Boolean expressions are statements that evaluate to either True or False. 

```
is_valid = True
has_mutation = False

# Simple boolean assignment
print(is_valid)      # Output: True
print(has_mutation)  # Output: False
```

## 6.2. Comparison operations

We have already seen this before. Comparison operators allow us to compare values and create boolean expressions. These are fundamental for creating conditions.

Here are some of the basic operators 

- == (equal to)
- != (not equal to)
- < (less than)
- > (greater than)
- <= (less than or equal to)
- >= (greater than or equal to)

## 6.3. If statements 

If statements are the fundamental control structure for making decisions in code. They execute different blocks of code based on conditions.

Here is an example of a basic syntax

```
if condition1:
    # code block 1
elif condition2:
    # code block 2
elif condition3:
    # code block 3
else:
    # default code block
```

You can apply this using a simple example as below:

```
age = 25

if age < 18:
    print("Child")
else:
    print("Adult")
```

or

```
age = 25

if age < 13:
    print("Child")
elif age < 20:
    print("Teenager")
else:
    print("Adult")
```

or 

```
mutation_count = 3
expression_level = 1.8

if mutation_count > 5:
    print("High genomic instability")
elif mutation_count > 2 **and** expression_level > 1.5:
    print("Moderate risk - close monitoring required")
else:
    print("Low risk - standard monitoring")
```

> [!NOTE]
> In Python, `and` returns True only if both conditions are True, while `or` returns True if at least one condition is True. 

## 6.4. Putting all together to make a a simple decision program

Simple decision programs combine conditionals, boolean expressions, and comparison operations without the complexity of functions. They execute a series of decisions in sequence to reach a conclusion.

Here is a generic example

```
# Simple program to categorize students based on scores
score = 85
attendance = 92
has_extra_credit = True

if score >= 90:
    grade = "A"
elif score >= 80:
    if attendance >= 90 and has_extra_credit:
        grade = "A"  # Boost grade due to good attendance and extra credit
    else:
        grade = "B"
elif score >= 70:
    grade = "C"
else:
    grade = "F"

print(f"Final grade: {grade}")  # Output: "Final grade: A"
```

but you can imagine that this kind of simple decision programmes can be applied in healthcare settings as well. 

Let's try an example below:

```
# Program to assess patient risk based on multiple biomarkers
tumor_size = 2.5          # in cm
lymph_nodes_involved = 1
hormone_receptor = True
her2_status = False

risk_level = ""
treatment_path = ""

# First assess basic risk factors
if tumor_size <= 2.0 and lymph_nodes_involved == 0:
    risk_level = "Low"
elif tumor_size <= 5.0 and lymph_nodes_involved <= 3:
    risk_level = "Intermediate"
else:
    risk_level = "High"

# Then determine treatment path based on risk and receptor status
if risk_level == "Low":
    if hormone_receptor:
        treatment_path = "Hormone therapy"
    else:
        treatment_path = "Active monitoring"
elif risk_level == "Intermediate":
    if hormone_receptor and her2_status:
        treatment_path = "Combined targeted therapy"
    elif hormone_receptor:
        treatment_path = "Hormone therapy + chemotherapy"
    else:
        treatment_path = "Chemotherapy"
else:  # High risk
    treatment_path = "Aggressive combined therapy"
```

Based on the code block below, could you guess what is the outcome? 

Run the code below to find out 

```
print(f"Risk Level: {risk_level}")         
print(f"Treatment Path: {treatment_path}")   
```
