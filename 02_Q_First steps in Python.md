## Basic Level questions

#### 1. Declare variables to store the following information and then print out their data types using `type`. You should try and use comments on your codes.

- Patient ID: 12345
- Patient Name: Sarah Chen
- Body Temperature: 37.2
- Is Fasting: True

  <details>
  <summary>Click to view answer</summary>

  ```
  # Declaring variables
  patient_id = 12345             
  patient_name = "Sarah Chen"    
  body_temp = 37.2              
  is_fasting = True

  # Printing data types
  print("Patient ID type:", type(patient_id))
  print("Patient Name type:", type(patient_name))
  print("Body Temperature type:", type(body_temp))
  print("Is Fasting type:", type(is_fasting))
  ```
  
  </details>



#### 2. Create a greeting message for a patient that includes their name and the gene being tested. Use an f-string.

- Patient Name: Sarah Chen
- Gene tested: BRCA1
- Message: Welcome <patient name>, we will be analyzing your <gene_tested>.

  <details>
  <summary>Click to view answer</summary>

  ```
  patient_name = "Sarah Chen"
  gene_tested = "BRCA1"
  print(f"Welcome {patient_name}, we will be analyzing your {gene_tested} gene variant today.")
  ```
  
  </details>
