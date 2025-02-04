## Basic Level Questions

#### 1. Write a function that takes a patient's temperature and returns whether they have a fever (above 37.5°C).

  <details>
  <summary>Click to view answer</summary>

  ```
  def check_fever(temperature):
      return temperature > 37.5
  ```
  
  </details>

#### 2. Create a function that calculates medication dosage based on patient weight (dosage = weight * 0.15).

  <details>
  <summary>Click to view answer</summary>

  ```
  def calculate_dosage(weight):
      dosage = weight * 0.15
      return dosage
  ```
  
  </details>


## Intermediate Level Questions

#### 3. Write a function to calculate patient's BMI (in 2 decimal places) based on users input of weight and height. 

  <details>
  <summary>Click to view answer</summary>

  ```
  def calculate_bmi(weight, height):
      bmi = weight / (height ** 2)
      return bmi

  # Get user input
  weight = float(input("Enter weight in kilograms: "))
  height = float(input("Enter height in meters: "))

  # Calculate and print result
  patient_bmi = calculate_bmi(weight, height)
  print(f"Patient's BMI is: {patient_bmi}")
  ```
  
  </details>

#### 4. Write a function that takes a patient's systolic and diastolic blood pressure and returns their status ("Normal", "Elevated", or "High").

  <details>
  <summary>Click to view answer</summary>

  ```
  def check_blood_pressure(systolic, diastolic):
      if systolic < 120 and diastolic < 80:
          return "Normal"
      elif systolic < 130 and diastolic < 80:
          return "Elevated"
      else:
          return "High"

  # Get user input
  systolic = float(input("Enter systolic pressure: "))
  diastolic = float(input("Enter diastolic pressure: "))

  # Calculate and print result
  blood_pressure = check_blood_pressure(systolic, diastolic)
  print(f"Patient's blood pressure is: {blood_pressure}")
  ```
  
  </details>
