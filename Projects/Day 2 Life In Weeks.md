### Question:

To create a program that calculates how many weeks you have left until age 90 based on your current age, you can follow these steps. Below is the Python code using f-strings and basic arithmetic operations:

### Steps to Solve:

1. **Input the age:**
   - Prompt the user to enter their current age using `input()`.

2. **Convert age to integer:**
   - Convert the input age from string to integer using `int()`.

3. **Calculate years left to live:**
   - Subtract the current age from 90 to find out how many years are left until age 90.

4. **Calculate weeks left:**
   - Assuming there are 52 weeks in a year, multiply the years left by 52 to get the total weeks left.

5. **Print the result:**
   - Use an f-string to format and print the message showing the calculated weeks left.

### Python Code:

```python
# Take the age as input from the user
age = input("Enter your current age: ")

# Convert the age into integer
age_as_int = int(age)

# Calculate the years left to live until age 90
years_left = 90 - age_as_int

# Calculate the weeks left to live assuming there are 52 weeks in a year
weeks_left = years_left * 52

# Print the message using f-string
print(f"You have {weeks_left} weeks left until you turn 90 years old.")
