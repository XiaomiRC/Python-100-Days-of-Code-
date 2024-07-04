# Instructions
You are painting a wall. The instructions on the paint can says that `1 can of paint can cover 5 square meters` of wall. Given a random height and width of wall, calculate how many cans of paint you'll need to buy.

- number of cans = (wall height x wall width) ÷ coverage per can.

```
e.g. Height = 2, Width = 4, Coverage = 5

number of cans = (2 * 4) / 5
               = 1.6
               
But because you can't buy 0.6 of a can of paint, the result should be rounded up to 2 cans.
```
**IMPORTANT:** Notice the name of the function and parameters must match those on line 13 for the code to work.
### Example Input
```
3
9
```
### Example Output
```
You'll need 6 cans of paint.
```
**Hint**
Stackoveflow link on how to round up a number: https://stackoverflow.com/questions/2356501/how-do-you-round-up-a-number-in-python

```python
# Print a message indicating the purpose of the program
print("This is a paint area calculator")

import math

# Define a function to calculate the number of paint cans needed
def paint_calc(height, width, cover):
    # Calculate the total area of the wall
    area = height * width
    
    # Calculate the number of cans needed, rounding up to ensure enough coverage
    no_of_cans = math.ceil(area / cover)
    
    # Print the result with a formatted string
    print(f"You'll need {no_of_cans} cans of paint.")

# Prompt the user to enter the dimensions of the wall
test_h = float(input("Enter the height of the wall in meters: ")) 
test_w = float(input("Enter the width of the wall in meters: ")) 

# Specify the coverage per can of paint
coverage = 5

# Call the paint_calc function with the provided dimensions and coverage
paint_calc(height=test_h, width=test_w, cover=coverage)

```
