# Question: Write a Python program that converts temperatures between Celsius and Fahrenheit.
 The program should prompt the user to enter a temperature and choose an operation:
- Press 1 to convert from Celsius to Fahrenheit
- Press 2 to convert from Fahrenheit to Celsius
 If the user selects an operation, the program should perform the conversion and print the result. 
 If an invalid choice is entered, it should display an error message.
Hint:
Formulas to convert:
1. Celsius to Farenheit is
```(0°C × 9/5) + 32 = 32°F```
2. Farenheit to Celsius is
```(32°F − 32) × 5/9 = 0°C```

### Solution:
``` python
print("Welcome to the Temperature converter\n")

# Prompt the user to enter the temperature
temp = float(input("Enter the temperature: "))

# Prompt the user to choose an operation
user_choice = int(input("Enter 1 to convert from Celsius to Fahrenheit\nEnter 2 to convert from Fahrenheit to Celsius\n"))

fahrenheit = 0
celsius = 0

# Check the user's choice and perform the corresponding conversion
if user_choice == 1:
    # Convert Celsius to Fahrenheit
    fahrenheit = (temp * 9/5) + 32
    print(f"The temperature in Fahrenheit is {fahrenheit}")
elif user_choice == 2:
    # Convert Fahrenheit to Celsius
    celsius = (temp - 32) * 5/9
    print(f"The temperature in Celsius is {celsius}")
else:
    # Print an error message for invalid input
    print("Invalid Input")
```
