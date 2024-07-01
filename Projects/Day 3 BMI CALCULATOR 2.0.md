# Create a BMI calculator which:
1. Takes the height in meters and weight in Kgs as input, calculates the BMI.
2. Tells the user the interpretation of their BMI based on the BMI value.
- i. Under 18.5 they are underweight
- ii. Equal to or over 18.5 but below 25 they have a normal weight
- iii. Equal to or over 25 but below 30 they are slightly overweight
- iv. Equal to or over 30 but below 35 they are obese
- v. Equal to or over 35 they are clinically obese.

**NOTE**
- BMI = weight ÷ height * height

```python
# Takes the height and weight as an input from the user
height = float(input("Enter your height in meters e.g., 1.55\n"))
weight = int(input("Enter your weight in kilograms e.g., 72\n"))

# Calculates the BMI
bmi = round(weight/(height**2))

# Conditions that provdives the clinical interpretation of the user's BMI
if bmi<18.5:
  print(f"Your BMI is {bmi}, you are underweight.")
elif bmi<25:
  print(f"Your BMI is {bmi}, you have a normal weight.")
elif bmi<30:
  print(f"Your BMI is {bmi}, you are slightly overweight.")
elif bmi<35:
  print(f"Your BMI is {bmi}, you are obese.")
else:
  print(f"Your BMI is {bmi}, you are clinically obese.")
```
