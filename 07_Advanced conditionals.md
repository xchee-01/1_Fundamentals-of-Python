# 7. Advanced conditionals

Let's look at some other slightly more complicated conditionals that you can apply. 

## 7.1 Nested conditionals

 Nested conditionals are if statements within if statements, allowing for more complex decision trees and finer control over program flow.

 They generally have a syntax as below:

 ```
if outer_condition:
    if inner_condition1:
        # code block 1
    else:
        # code block 2
else:
    if inner_condition2:
        # code block 3
    else:
        # code block 4
```

Here is an example of how this is applied in a generic setting

```
age = 25
has_license = True

if age >= 18:
    if has_license:
        print("Can drive alone")
    else:
        print("Need to get a license first")
else:
    if age >= 16:
        print("Can get a learner's permit")
    else:
        print("Too young to drive")
```

and how this can be applied in a medical setting

```
mutation_present = True
drug_resistance = False
tumor_size = 2.5  # cm

if mutation_present:
    if drug_resistance:
        if tumor_size > 3:
            print("Recommend surgical intervention")
        else:
            print("Try alternative therapy")
    else:
        print("Proceed with standard treatment")
else:
    print("Continue with regular monitoring")
```

## 7.2 Switch-case equivalent 

Match statements, introduced in Python 3.10+, provide a cleaner way to handle multiple conditions based on a single value, similar to switch-case in other languages.

The basic syntax of match statements are as below 

```
match value:
    case pattern1:
        # code block 1
    case pattern2:
        # code block 2
    case _:
        # default code block
```

We can do simple value matching such as the example below:

```
Switch-Case Equivalent (Match Statements) in Python - Expanded Guide
Introduction
Match statements are Python's answer to switch-case statements found in other programming languages. They provide a cleaner and more powerful way to handle multiple conditional branches based on a single value.
Basic Pattern Matching
Simple Value Matching
pythonCopystatus_code = 404

match status_code:
    case 200:
        print("Success!")
    case 404:
        print("Not Found")
    case 500:
        print("Server Error")
    case _:
        print("Unknown Status Code")
```

> [!NOTE]
> The underscore (_) is used as a wildcard to catch all unmatched cases

or multiple values in one case

```
day = "Monday"

match day:
    case "Monday" | "Tuesday" | "Wednesday":
        print("Beginning of the week")
    case "Thursday" | "Friday":
        print("End of the week")
    case "Saturday" | "Sunday":
        print("Weekend")
    case _:
        print("Invalid day")
```

> [!NOTE]
> The `|` in Python is a bitwise OR operator.
> In pattern matching (match statements), you need to use the | operator instead of or. This is because | here is acting as a pattern separator rather than a logical operator.

You can apply this in precision medicine such as the example below

```
mutation_type = "deletion"

match mutation_type:
    case "insertion" | "duplication":
        print("DNA sequence length increased")
        print("Check for frameshift effects")
    case "deletion" | "loss":
        print("DNA sequence length decreased")
        print("Assess protein truncation")
    case "missense":
        print("Amino acid substitution")
        print("Evaluate protein function impact")
    case "silent":
        print("No amino acid change")
        print("Check for splicing effects")
    case _:
        print("Unknown mutation type")
        print("Further analysis needed")
```
