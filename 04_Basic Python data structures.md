# 4. Basic Python data structures 

Python data structures are containers that store and organize data, with built-in types like lists, tuples, dictionaries, and sets that each have specific ways of storing and accessing data for different use cases.

## 4.1. Lists

Lists are ordered, mutable sequences that can store multiple items of different data types. They are one of the most versatile and commonly used data structures in Python.

```
# Creating lists
my_list = [1, 2, 3, 4, 5]
mixed_list = [1, "hello", 3.14, True]
```

We can use some methods on lists

```
# Common list operations
my_list.append(6)        # Add element
my_list.remove(3)        # Remove element
my_list.insert(2, 10)    # Insert at position
my_list.pop()           # Remove and return last element
length = len(my_list)    # Get length
```

> [!NOTE]  
> After running a method, for example,
>
> ```
> my_list.append(6)
> ```
>
> You should type my_list to view the output
>
> ```
> my_list
> ```

Here is how we can apply these in Precision Medicine

```
# Managing patient genetic markers
patient_markers = ["BRCA1", "TP53", "EGFR"]
patient_markers.append("KRAS")
print(f"Genetic markers to analyze: {patient_markers}")
print(f"Primary marker: {patient_markers[0]}")
```

## 4.2. Dictionaries

Dictionaries are unordered collections of key-value pairs, perfect for storing related information and creating mappings between data. They provide fast lookups and are highly efficient for data organization.

We can create dictionaries like this

```
# Creating dictionaries
my_dict = {"name": "John", "age": 30}
```

And we can access the elements in the dictionaries like this

```
# Common dictionary operations
my_dict["city"] = "New York"    # Add/update key-value
del my_dict["age"]             # Delete key-value
value = my_dict.get("name")    # Safe value access
keys = my_dict.keys()          # Get all keys
```

And we may apply this in the medical setting, for example, extracting patient mutation profile. 

```
# Managing patient mutation profiles
patient_mutations = {
    "BRCA1": "pathogenic",
    "TP53": "benign",
    "EGFR": "variant_of_unknown_significance"
}
print(f"BRCA1 status: {patient_mutations['BRCA1']}")
```

## 4.3. Tuples

Tuples are **immutable** sequences that cannot be changed after creation. They are perfect for storing fixed collections of items and are more memory efficient than lists.

> [!NOTE]  
> Immutability means that once a value or object is created, it cannot be changed (mutated) - any operations that seem to modify it actually create a new copy instead. This helps prevent bugs and makes code easier to reason about since you know values won't unexpectedly change.

You can create tuples like this:

```
# Creating tuples
my_tuple = (1, 2, 3)
single_tuple = (1,)    # Note the comma
```

Here are some methods that can be applied onto a tuple

```
# Common tuple operations
length = len(my_tuple)
element = my_tuple[0]
```

You can also apply this into medical dataset.

```
# Storing gene coordinates
gene_location = ("chromosome_7", 55019017, 55211628)
print(f"Gene starts at position: {gene_location[1]}")
```

## 4.4. Sets

Sets are unordered collections of unique elements. They are perfect for removing duplicates and performing mathematical set operations like unions and intersections.

You can create sets like this:

```
# Creating sets
my_set = {1, 2, 3, 4}
my_set.add(5)           # Add element
my_set.remove(2)        # Remove element
```

You can think of sets like a Venn Diagram. Therefore, we can do similar mathematical operations as you would on a set. 

```
# Set operations
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union = set1 | set2
intersection = set1 & set2
```

Here is an example of how you would apply this in a molecular medicine context. 

```
# Managing unique patient mutations
patient_variants = {"rs334", "rs328", "rs324"}
new_variants = {"rs324", "rs335"}
all_variants = patient_variants | new_variants
common_variants = patient_variants & new_variants
print(f"All unique variants: {all_variants}")
```
