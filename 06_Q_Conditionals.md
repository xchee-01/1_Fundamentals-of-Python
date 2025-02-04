## Basic Level Questions

#### 1. Write a simple conditional statement that prints "High Expression" if a gene expression value is greater than 2.0, and "Normal Expression" otherwise. Ask the users to input the expression value. 

  <details>
  <summary>Click to view answer</summary>

  ```
  # Ask user for gene expression value
  expression_value = float(input('What is the gene expression value?'))

  # If statement
  if expression_value > 2.0:
      print("High Expression")
  else:
      print("Normal Expression")
  ```
  
  </details>

#### 2. Write code that prints "Treatment Eligible" if both age is greater than 18 AND tumour_size is greater than 1.0 cm. Ask the users to input the age and tumour_size. 

  <details>
  <summary>Click to view answer</summary>

  ```
  age = float(input('What is age of patient?'))
  tumor_size = float(input('What is the tumour size?'))

  if age > 18 and tumor_size > 1.0:
      print("Treatment Eligible")
  else:
      print("Treatment Ineligible")
  ```
  
  </details>

## Intermediate Level Questions

#### 3. Create a programme that classifies tumor stages (I, II, or III) based on the user's input or tumour size and number of lymph nodes. 

- **Stage I: tumor_size < 2.0 and no lymph node involvement**
- **Stage II: tumor_size between 2.0 and 5.0 or limited lymph node involvement**
- **Stage III: everything else**

  <details>
  <summary>Click to view answer</summary>

  ```
  tumor_size = float(input('What is the tumour size?'))
  lymph_nodes = float(input('How many lymph nodes are there?'))

  if tumor_size < 2.0 and lymph_nodes == 0:
      print("Stage I")
  elif (tumor_size >= 2.0 and tumor_size <= 5.0) or lymph_nodes <= 3:
      print("Stage II")
  else:
      print("Stage III")
  ```
  
  </details>

#### 4. Create a program that determines clinical trial eligibility based on multiple criteria:

- **Patient must be > 18 years old**
- **Must have specific mutation (BRAF_mutation = True)**
- **Must have adequate blood counts (blood_count > 1000)**
- **Must not have had previous treatment (previous_treatment = False)**

**Would this patient with the following profile qualify?**

```
age = 45
BRAF_mutation = True
blood_count = 1200
previous_treatment = False
```

  <details>
  <summary>Click to view answer</summary>
    
  ```
  age = 45
  BRAF_mutation = True
  blood_count = 1200
  previous_treatment = False

  if (age > 18 and 
      BRAF_mutation and 
      blood_count > 1000 and 
      not previous_treatment):
      print("Eligible for Clinical Trial")
  else:
      print("Not Eligible for Clinical Trial")
  ```
  
  </details>

## Advanced Level Questions

#### 5. You're developing a precision medicine program for a lung cancer clinic. Create a program that determines treatment eligibility and recommended first-line therapy based on patient data. You are to generate a report for the doctor to read. 

**Treatment criteria:**

- **If performance status > 2, only supportive care is recommended**
- **For EGFR mutation positive: Recommend EGFR TKI if no prior TKI treatment**
- **For ALK positive: Recommend ALK TKI if no prior TKI treatment**
- **For PD-L1 > 50%: Consider immunotherapy if no activating mutations**
- **For all others: Consider chemotherapy if performance status <= 2**

**This is the patient data**

```
# Patient data
age = 65
smoking_status = "never"    
EGFR_mutation = False
ALK_fusion = False
PDL1_level = 60
performance_status = 1
prior_TKI = False
```

**The expected report should have this *exact* format**

```
Patient Profile:
Age: 65
Smoking Status: former
EGFR Mutation: False
ALK Fusion: False
PD-L1 Level: 60%
Performance Status: 1

Recommended Treatment: Immunotherapy
```

  <details>
  <summary>Click to view answer</summary>
    
  ```
  # Patient data
  age = 65
  smoking_status = "former"    # can be "current", "former", or "never"
  EGFR_mutation = False
  ALK_fusion = False
  PDL1_level = 60
  performance_status = 1
  prior_TKI = False

  # Decision tree for treatment recommendation
  if performance_status > 2:
      treatment = "Supportive care only"
  elif EGFR_mutation and not prior_TKI:
      treatment = "EGFR TKI therapy"
  elif ALK_fusion and not prior_TKI:
      treatment = "ALK TKI therapy"
  elif PDL1_level > 50 and not (EGFR_mutation or ALK_fusion):
      treatment = "Immunotherapy"
  else:
      treatment = "Chemotherapy"

  # Print patient profile and recommendation
  print("Patient Profile:")
  print(f"Age: {age}")
  print(f"Smoking Status: {smoking_status}")
  print(f"EGFR Mutation: {EGFR_mutation}")
  print(f"ALK Fusion: {ALK_fusion}")
  print(f"PD-L1 Level: {PDL1_level}%")
  print(f"Performance Status: {performance_status}")
  print(f"\nRecommended Treatment: {treatment}")
  ```
  
  </details>
