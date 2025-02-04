## Basic Level Questions

#### 1. Given this list of gene markers:

```
markers = ["BRCA1", "TP53", "EGFR", "KRAS"]
```

**Write code to:**
- **Add "BRAF" to the end**
- **Remove "TP53"**
- **Print the first marker**
- **Print the total number of markers**

  <details>
  <summary>Click to view answer</summary>

  ```
  markers.append("BRAF")
  markers.remove("TP53")
  print(markers[0])  
  print(len(markers)) 
  ```
  
  </details>

#### 2. Given this mutation profile:

```
mutation_profile = {
    "BRCA1": "pathogenic",
    "TP53": "benign",
    "EGFR": "unknown"
}
```

**Write code to:**
- **Add a new mutation "BRAF" with status "pathogenic"**
- **Print the status of BRCA1**
- **Check if "KRAS" exists in the profile**

> [!TIP]
> You may refer back to the learning materials or [here](https://www.geeksforgeeks.org/python-dictionary/)

  <details>
  <summary>Click to view answer</summary>

  ```
  mutation_profile["BRAF"] = "pathogenic"
  print(mutation_profile["BRCA1"])  
  print("KRAS" in mutation_profile)  
  ```
  
  </details>

## Intermediate Level Questions

#### 3. You have two sets of variants found in different populations:

```
population_a_variants = {"rs334", "rs328", "rs324"}
population_b_variants = {"rs324", "rs335", "rs334"}
```

**Write code to find:**
- **Variants present in both populations**
- **All unique variants across both populations**
- **Variants unique to population A**

> [!TIP]
> You may refer back to the learning materials or [here](https://www.geeksforgeeks.org/sets-in-python/)

  <details>
  <summary>Click to view answer</summary>

  ```
  common_variants = population_a_variants & population_b_variants
  all_variants = population_a_variants | population_b_variants
  unique_to_a = population_a_variants - population_b_variants

  print(common_variants)  
  print(all_variants)    
  print(unique_to_a)     
  ```
  
  </details>

## Advanced Level Questions

#### 4. You have a DNA sequence from a small part of a gene. Your task is to translate segments of this sequence into amino acids using a simplified codon table.

```
dna_codons = ["ATG", "TGG", "GAG", "TAC", "CAG"]
```

Your desired output at the end of the code would be:

```
['Amino acid 1', 'Amino acid 2', 'Amino acid 3', 'Amino acid 4', 'Amino acid 5']
```

> [!TIP]
> 1. Create a dictionary of DNA codons and their corresponding amino acids. Refer to a DNA codon table
> 2. Create a list of codons as per the list shown in the question above
> 3. Translate the five codons using the dictionary and add them to your amino acids list
> 4. Print your results 

  <details>
  <summary>Click to view answer</summary>

  ```
  # Create dictionary mapping codons to amino acids
  codon_table = {
      "ATG": "Methionine",
      "TGG": "Tryptophan",
      "GAG": "Glutamic_acid",
      "TAC": "Tyrosine", 
      "CAG": "Glutamine"
  }

  #Create the list of codons
  dna_codons = ["ATG", "TGG", "GAG", "TAC", "CAG"]

  # Create empty list for amino acids
  amino_acids = []

  # Add each translated codon
  amino_acids.append(codon_table[dna_codons[0]])
  amino_acids.append(codon_table[dna_codons[1]])
  amino_acids.append(codon_table[dna_codons[2]])
  amino_acids.append(codon_table[dna_codons[3]])
  amino_acids.append(codon_table[dna_codons[4]])

  print(amino_acids)
  ```
  
  </details>
