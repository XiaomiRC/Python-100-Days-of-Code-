### Write a Python program that calculates and displays the diameter, area, and circumference of a circle based on the radius entered by the user. Ensure the program handles cases where the radius is not a positive integer by providing appropriate feedback to the user.

### Solution:
```python
# Display a welcome message to the user
print("Welcome to the Circle Dimension Calculator!")

# Prompt the user to enter the radius of the circle
radius = int(input("Enter the radius of the circle:\n"))

# Define the value of pi
pi = 3.14159265359

# Check if the radius is greater than 0
if radius > 0:
    # Calculate and round the diameter of the circle
    diameter = round(2 * radius, 2)
    
    # Calculate and round the area of the circle
    area = round(pi * radius ** 2, 2)
    
    # Calculate and round the circumference of the circle
    circumference = round(2 * pi * radius, 2)
    
    # Print the calculated dimensions of the circle
    print("Diameter:", diameter)
    print("Area:", area)
    print("Circumference:", circumference)
else:
    # Inform the user if the input radius is not valid
    print("Invalid input. Please enter a positive integer for the radius.")

```
