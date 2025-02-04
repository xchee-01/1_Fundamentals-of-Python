## Basic Level Questions

#### 1. What is the result of this code?

```
mutation_status = True 
if mutation_status:
    print("Mutation detected")
else:
    print("No mutation found")
```

  <details>
  <summary>Click to view answer</summary>

  ```
  "Mutation detected" will be printed. 
  ```
  
  </details>

#### 2. Given this code, what would be printed if patient_age = 15?

```
patient_age = 15
if patient_age < 18:
    print("Pediatric protocol")
else:
    print("Adult protocol")
```

  <details>
  <summary>Click to view answer</summary>

  ```
  "Pediatric protocol" will be printed 
  ```
  
  </details>

## Intermediate Level Questions

#### 3. What will this nested conditional print if mutation_present = True and drug_resistance = False?

```
if mutation_present:
    if drug_resistance:
        print("Consider alternative therapy")
    else:
        print("Standard therapy recommended")
else:
    print("No targeted therapy needed")
```

  <details>
  <summary>Click to view answer</summary>

  ```
  "Standard therapy recommended" will be printed 
  ```
  
  </details>

#### 4. What will this nested conditional print if gene_expression = "high" and methylation = True?

```
if gene_expression == "high":
    if methylation:
        print("Epigenetic modification detected")
    else:
        print("Standard expression pattern")
else:
    print("Low expression level")
```

  <details>
  <summary>Click to view answer</summary>

  ```
  "Epigenetic modification detected" will be printed 
  ```
  
  </details>

#### 5. Given these values: tumor_type = "carcinoma" and p53_status = "mutated", what would the output be?

```
if tumor_type == "carcinoma":
    if p53_status == "mutated":
        print("High risk - consider aggressive treatment")
    else:
        print("Standard treatment protocol")
else:
    if p53_status == "mutated":
        print("Monitor closely")
    else:
        print("Regular follow-up")
```

  <details>
  <summary>Click to view answer</summary>

  ```
  "High risk - consider aggressive treatment" will be printed 
  ```
  
  </details>

#### 6. What will be printed for biomarker = "HER2" and level = "overexpressed"?

```
match (biomarker, level):
    case ("HER2", "overexpressed"):
        print("Consider targeted therapy")
    case ("HER2", "normal"):
        print("Standard protocol")
    case ("PDL1", "high"):
        print("Immunotherapy candidate")
    case _:
        print("No specific recommendations")
```

  <details>
  <summary>Click to view answer</summary>

  ```
  "Consider targeted therapy" will be printed 
  ```
  
  </details>
