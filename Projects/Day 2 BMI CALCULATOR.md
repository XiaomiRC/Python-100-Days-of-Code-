# Create a BMI calculator which takes the height in meters and weight in Kgs as input, calculates the BMI and provides the output as an integer.

[NOTE] BMI = weight ÷ height *  height

```
# 1st input: enter height in meters e.g: 1.65
height = input()

# 2nd input: enter weight in kilograms e.g: 72
weight = input()

#Convert the height into float and the weight into integer
height_as_float = float(height)
weight_as_int = int(weight)

#BMI formula
bmi = weight_as_int / height_as_float**2

#Convert the BMI from decimal into whole number
bmi_as_int = int(bmi)
print(bmi_as_int)

```
