### Question:
Create a Python program that calculates the Body Mass Index (BMI) using the formula:
- BMI = weight ÷ height * height
  
where:
- `weight` is in kilograms (Kgs),
- `height` is in meters.

Write a program that:
1. Takes user input for `height` in meters and `weight` in kilograms.
2. Calculates the BMI using the provided formula.
3. Converts the calculated BMI from a decimal into an integer.
4. Prints the integer value of the BMI.

### Steps to Solve:

1. **Input height and weight:**
   - Use `input()` to prompt the user to enter the height in meters (`height`) and weight in kilograms (`weight`).

2. **Convert input values:**
   - Convert `height` from string to float (`height_as_float = float(height)`).
   - Convert `weight` from string to integer (`weight_as_int = int(weight)`).

3. **Calculate BMI:**
   - Compute BMI using the formula `bmi = weight_as_int / (height_as_float ** 2)`.

4. **Convert BMI to integer:**
   - Convert the computed BMI (`bmi`) from float to integer (`bmi_as_int = int(bmi)`).

5. **Print the BMI:**
   - Display the calculated BMI as an integer using `print(bmi_as_int)`.

### Python Code:

```python
# Input height in meters
height = input("Enter your height in meters (e.g., 1.65): ")

# Input weight in kilograms
weight = input("Enter your weight in kilograms (e.g., 72): ")

# Convert height to float and weight to integer
height_as_float = float(height)
weight_as_int = int(weight)

# Calculate BMI
bmi = weight_as_int / (height_as_float ** 2)

# Convert BMI to integer
bmi_as_int = int(bmi)

# Print the BMI
print(bmi_as_int)

