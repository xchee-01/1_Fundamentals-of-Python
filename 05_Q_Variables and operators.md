## Basic Level Questions

#### 1. What's wrong with these variable names in a medical analysis script?

```
p = 45        # patient age
dna = "ATCG"  # DNA sequence
t = 37.2      # temperature
```

  <details>
  <summary>Click to view answer</summary>

  ```
  #These variable names are too short and non-descriptive. Better names would be:

  patient_age = 45
  dna_sequence = "ATCG"
  body_temperature = 37.2
  ```
  
  </details>

## Intermediate Level Questions

#### 2. Given these tumor measurements over time, write code to calculate the percentage change:

```
initial_size = 3.2  # cm
current_size = 2.1  # cm
```

  <details>
  <summary>Click to view answer</summary>

  ```
  percentage_change = ((current_size - initial_size) / initial_size) * 100
  ```

  </details>

#### 3. Given three biomarker levels, write code using logical operators to determine if a patient meets clinical trial criteria. Write a code that will tell you TRUE if all conditions are met and FALSE if the conditions are not

```
protein_a_level = 45  # ng/mL
protein_b_level = 12  # ng/mL
protein_c_level = 89  # ng/mL

PROTEIN_A_THRESHOLD = 50
PROTEIN_B_THRESHOLD = 15
PROTEIN_C_THRESHOLD = 75
```

  <details>
  <summary>Click to view answer</summary>

  ```
  meets_criteria = (protein_a_level < PROTEIN_A_THRESHOLD and 
                 protein_b_level < PROTEIN_B_THRESHOLD and 
                 protein_c_level > PROTEIN_C_THRESHOLD)
  ```

  </details>

#### 4. Calculate the combined drug effectiveness score using operator precedence

```
efficacy = 0.85    
toxicity = 0.15   
duration = 12     
```

**The formula is**

```
score = (efficacy - toxicity) * (duration/24) + (1 - toxicity)
```

  <details>
  <summary>Click to view answer</summary>

  ```
  score = (efficacy - toxicity) * (duration/24) + (1 - toxicity)
  ```

  </details>

## Advanced Level Questions

You are working in a precision medicine clinic that monitors patients on targeted therapy. The clinic needs a system to generate alerts when patient metrics fall outside acceptable ranges. Generate appropriate alert flags using comparison and logical operators. 

```
# System thresholds (constants)
CRITICAL_TUMOR_INCREASE = 20     # % increase that triggers alert
MIN_IMMUNE_RESPONSE = 75         # minimum acceptable immune score
MAX_TOXICITY_LEVEL = 2.5        # maximum acceptable toxicity
MIN_PLATELET_COUNT = 150        # minimum platelet count (thousands/µL)
MAX_ALT_LEVEL = 50             # maximum ALT liver enzyme level (U/L)
MIN_DRUG_CONCENTRATION = 0.4    # minimum drug concentration in blood (µg/mL)

# Patient's current data
tumor_change_percent = -9.5     # negative means shrinkage
immune_response = 82            # score out of 100
toxicity_level = 1.8           # scale of 0-5
platelet_count = 145           # thousands/µL
alt_level = 65                 # U/L
drug_concentration = 0.38      # µg/mL
```

**You will need to create alert flags for** 

- **tumor_alert**
- **immune_alert**
- **toxicity_alert**
- **platelet_alert**
- **liver_alert**
- **drug_level_alert**
- **urgent_attention_needed (True if 2 or more alerts are True)**

> [!TIP]
> 1. First, create each alert separately by comparing the patient's values with their respective thresholds (eg. tumor_change_percent > CRITICAL_TUMOR_INCREASE).
> 2. Count how many individual alerts are rue. You may use `sum()`. Remember that `sum()` only counts how many `TRUE` there are in a list.
> 3. Set urgent_attention_needed to True if 2 or more alerts exist

  <details>
  <summary>Click to view answer</summary>

  ```
  # Generate individual alert flags
  tumor_alert = tumor_change_percent > CRITICAL_TUMOR_INCREASE
  immune_alert = immune_response < MIN_IMMUNE_RESPONSE
  toxicity_alert = toxicity_level > MAX_TOXICITY_LEVEL
  platelet_alert = platelet_count < MIN_PLATELET_COUNT
  liver_alert = alt_level > MAX_ALT_LEVEL
  drug_level_alert = drug_concentration < MIN_DRUG_CONCENTRATION

  # Count how many alerts are True using sum() and convert boolean to int
  alert_count = sum([tumor_alert, immune_alert, toxicity_alert, 
                  platelet_alert, liver_alert, drug_level_alert])

  # Generate urgent attention flag if 2 or more alerts are True
  urgent_attention_needed = alert_count >= 2
  ```

  </details>
