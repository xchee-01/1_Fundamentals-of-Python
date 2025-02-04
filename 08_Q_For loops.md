## Basic Level Questions

#### 1. What would be the output of this code?

```
mutations = ["A123T", "G45S", "P89L"]
for mutation in mutations:
    print(mutation)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  #The code will print:
  A123T
  G45S
  P89L
  ```
  
  </details>

#### 2. Write a for loop to print numbers from 0 to 4 using range().

  <details>
  <summary>Click to view answer</summary>

  ```
  for i in range(5):
      print(i)
  ```

  </details>


#### 3. How would you modify this code to print each amino acid with its position?

```
amino_acids = ["Gly", "Ala", "Val"]
```

**The intended output should look like this**
```
0: Gly
1: Ala
2: Val
```

  <details>
  <summary>Click to view answer</summary>

  ```
  for index, acid in enumerate(amino_acids):
      print(f"Position {index}: {acid}")
  ```

  </details>

## Intermediate Level Questions

#### 4. Create a code that converts DNA sequence to RNA using the for loop

> [!TIP]
> You can use `replace()`. You may read more [here](https://www.geeksforgeeks.org/python-string-replace/)

  <details>
  <summary>Click to view answer</summary>

  ```
  dna_sequence = ["ATCG", "GGCT", "TATA"]

  for nucleotides in dna_sequence: 
    RNA = nucleotides.replace('T', 'U')
    print(RNA)
  ```

  </details>

#### 5. Refering back to Question 4 above, write a code that converts DNA to RNA using list comprehension. 

  <details>
  <summary>Click to view answer</summary>

  ```
  rna_sequence = [seq.replace('T', 'U') for seq in dna_sequence]
  ```

  </details>

#### 6. Write a loop that filters and processes protein sequences containing specific motifs:

```
sequences = ["MGKTAS", "PGKTLS", "MAKVET"]
motif = "GKT"
```

> [!TIP]
> You may read up more on how to do this [here](https://www.geeksforgeeks.org/check-if-string-contains-substring-in-python/)

  <details>
  <summary>Click to view answer</summary>

  ```
  for sequence in sequences:
   if motif in sequence:
     print(sequence)
  ```

  </details>

## Advanced Level Questions

#### 7. You are analyzing clinical trial data for a targeted therapy drug trial. You have data from 10 patients who received different doses of the drug. For each patient, you have:

- **Initial tumor size (in mm)**
- **Tumor size after treatment (in mm)**
- **Drug concentration in blood (in ng/mL)**
- **Mutation status (True/False for presence of target mutation)**

**Your tasks:**

- **Calculate the percentage change in tumor size for each patient**
- **Identify which patients are responders (defined as tumor shrinkage > 30%)**
- **Find the average drug concentration among responders**

```
# Patient data stored as lists
initial_sizes = [45, 32, 50, 28, 65, 40, 55, 48, 35, 42]
final_sizes = [20, 28, 48, 15, 60, 38, 25, 45, 30, 40]
drug_concentrations = [150, 100, 80, 120, 90, 110, 140, 95, 105, 88]
mutation_status = [True, False, False, True, False, False, True, False, True, False]
```

  <details>
  <summary>Click to view answer</summary>

  ```
    responders = []
    drug_concentrations_of_responders = []
    mutation_status_of_responders = []

    for index in range(len(initial_sizes)):
      size_difference = initial_sizes[index] - final_sizes[index]
      percentage_change = (size_difference / initial_sizes[index]) * 100

      if percentage_change > 30:
        responders.append(index)

    for responders_index in responders:
      drug_concentrations_of_responders.append(drug_concentrations[responders_index])

    response_rate = len(responders) / len(initial_sizes) * 100
    avg_concentration = sum(drug_concentrations_of_responders) /len(drug_concentrations_of_responders)

    print(f"Overall response rate: {response_rate}%")
    print(f"Average drug concentration in responders: {avg_concentration:.2f} ng/mL")
  ```

  </details>


