## Basic Level Questions

#### 1. What will be the output of the following code?

```
patient_name = "Jane Smith"
diagnosis = "TP53 mutation"
print(f"Patient {patient_name} is being tested for {diagnosis}")
```

  <details>
  <summary>Click to view answer</summary>

  ```
  The output will be: "Patient Jane Smith is being tested for BRCA1 mutation"
  ```
  
  </details>

#### 2. Given this code, what happens if you print the type of `expression_value`?

  <details>
  <summary>Click to view answer</summary>

  ```
  It will print <class 'str'> because the value is enclosed in quotes, making it a string despite looking like a number.
  ```
  
  </details>

#### 3. If you have a DNA sequence "ATCGATCG", how would you count the number of 'A' nucleotides? Write a code that can count the number of As inside the gene sequence

> [!TIP]
> You may refer back to the learning materials or [here](https://www.w3schools.com/python/ref_string_count.asp)

  <details>
  <summary>Click to view answer</summary>

  ```
  sequence = "ATCGATCG"
  a_count = sequence.count('A')
  ```
  
  </details>

## Intermediate Level Questions

#### 4. Given a mutation probability of 0.0034, write code to convert it to scientific notation for publication. Write a code that will convert 0.0034 to a scientific notation.

> [!TIP]
> You may refer to [here](https://rowannicholls.github.io/python/intro/f_strings.html)

  <details>
  <summary>Click to view answer</summary>

  ```
  probability = 0.0034
  scientific_notation = f"{probability:.2e}"
  ```
  
  </details>

#### 5. How would you check if a patient's gene expression value is within a clinically significant range (between 2.0 and 4.0)? Write a code that will:

**(a) ask you for the patient's gene expression value**
**(b) store a TRUE or FALSE if the patient's gene expression falls in the range of 2.0 to 4.0**

> [!TIP]
> You will need to use the `input()` function. 
> You may refer to [here](https://www.geeksforgeeks.org/taking-input-in-python/)
> Equally important for you to take note is that the input is in str format.
> So you would need to convert it into float first. 


  <details>
  <summary>Click to view answer</summary>

  ```
  expression_value = float(input("What is the gene expression value of the patient? "))
  is_significant = 2.0 <= expression_value <= 4.0
  is_significant 
  ```
  
  </details>

## Advanced Level Questions

#### 6. Write a piece of code that will calculate the melting temperature of a primer. The formula for calculating a primer is given by: 

```
Tm = 64.9 + 41 * (G + C - 16.4) / (A + T + G + C)
```

> [!TIP] 
> 1. ask user for the sequence of the input primer 
> 2. calculate the As, Ts, Gs and Cs,
> 3. plug the values into the formula 
> 4. print out the melting temperature, Tm, to the user

  <details>
  <summary>Click to view answer</summary>

  ```
  #Get primer sequence from user
  primer = input("Please enter your primer sequence: ")

  #Count nucleotides
  a_count = primer.count('A')
  t_count = primer.count('T')
  g_count = primer.count('G')
  c_count = primer.count('C')

  #Calculate melting temperature using the formula
  tm = 64.9 + (41 * (g_count + c_count - 16.4) / (a_count + t_count + g_count + c_count))

  #Print the result
  print(f"\nThe melting temperature (Tm) is: {tm:.1f}°C")
  ```

  </details>


