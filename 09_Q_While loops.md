## Basic Level Questions

#### 1. What output will the following code produce?

```
mutation_count = 3
while mutation_count > 0:
    print(f"Remaining mutations: {mutation_count}")
    mutation_count -= 1
```

  <details>
  <summary>Click to view answer</summary>

  The output will be:
  
  ```
  Remaining mutations: 3
  Remaining mutations: 2
  Remaining mutations: 1
  ```
  
  </details>

#### 2. Write a while loop that prints gene expression levels starting from 100 and halving each time until it goes below 10.

  <details>
  <summary>Click to view answer</summary>

  ```
  expression = 100
  while expression >= 10:
      print(f"Expression level: {expression}")
      expression = expression / 2
  ```
  
  </details>

## Intermediate Level Questions

#### 3. Complete the following code to validate drug dosage input (valid range: 0-1000mg). If users key in drug dosage from 0-1000mg, the code will output "Valid dosage entered". If not, then it will print "Dosage must be between 0 and 1000mg". 

  <details>
  <summary>Click to view answer</summary>
  
  ```
    while True:
      dosage = float(input("Enter drug dosage (mg): "))
      if 0 <= dosage <= 1000:
         print("Valid dosage entered")
         break
      else:
        print("Dosage must be between 0 and 1000 mg")
  ```
  
  </details>

## Advanced Level Questions

#### 4. You are analyzing DNA sequences for specific regulatory motifs. Write a program that:

- **Asks the user for a DNA sequence**
- **Asks for a motif to search for**
- **Reports all positions where the motif occurs in the sequence**

> [!TIP]
> Here's some hints on how you can tackle this question
> 1. Get user input for DNA sequence and motif. Convert both to uppercase.
> 2. Create two counters: position (start at 0) and found_count (start at 0).
> 3. Loop while position ≤ sequence_length - motif_length.
> 4. Take a slice of sequence starting at current position, with length = motif_length.
> 5. If slice matches motif: print position and add 1 to found_count.
> 6. Add 1 to position for next loop iteration.
> 7. Print total matches found.

  <details>
  <summary>Click to view answer</summary>
  
  ```
    # Get input from user
    sequence = input("Enter DNA sequence (e.g., ATCGGGCTATAA): ").upper()
    motif = input("Enter motif to search for (e.g., GGC): ").upper()

    # Initialize variables
    position = 0
    found_count = 0

    # Search through the sequence
    while position <= len(sequence) - len(motif):
        # Extract the subsequence to compare
        current_subsequence = sequence[position:position + len(motif)]
    
        # Check if we found a match
        if current_subsequence == motif:
            print(f"Match found at position {position}")
            found_count += 1
            
        position += 1

    # Report final results
    if found_count == 0:
        print("No matches found.")
    else:
        print(f"Total matches found: {found_count}")
  ```
  
  </details>
