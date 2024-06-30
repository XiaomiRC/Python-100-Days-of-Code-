### Question:

Create a Tip Calculator that calculates the amount each person needs to pay, including a specified tip percentage(10, 12, or 15), when dining out with friends at a restaurant.

### What the Calculator Should Do:

When given inputs such as the total bill amount, the desired tip percentage, and the number of people splitting the bill:
1. Calculate the total tip amount based on the specified percentage(10, 12, or 15).
2. Add the total tip amount to the original bill to get the final amount to be split.
3. Divide the final amount by the number of people and round the result to 2 decimal places.
4. Print out how much each person should pay.

### Steps to Solve:

1. **Print a welcoming message:**
   - Use `print("Welcome to the tip calculator!")` to greet the user.

2. **Input the bill amount, tip percentage, and number of people:**
   - Use `float(input("What was the total bill? $"))` to prompt the user to enter the total bill amount.
   - Use `int(input("How much percent of the bill would you like to give as tip? 10, 12, or 15? "))` to ask for the tip percentage.
   - Use `int(input("How many people to split the bill? "))` to ask for the number of people splitting the bill.

3. **Calculate the total tip amount:**
   - Compute `total_tip_amount = bill * (tip / 100)` to determine the tip amount based on the input percentage.

4. **Calculate the final amount per person:**
   - Compute `final_amount = round((bill + total_tip_amount) / people, 2)` to calculate the amount each person needs to pay after adding the tip and dividing by the number of people, rounded to 2 decimal places.

5. **Print the result:**
   - Use an f-string (`print(f"Each person should pay: ${final_amount}")`) to display how much each person should pay.

### Python Code:

```python
# Print a welcoming message
print("Welcome to the tip calculator!")

# Ask the user to provide inputs
bill = float(input("What was the total bill? $"))
tip = int(input("How much percent of the bill would you like to give as tip? 10, 12, or 15? "))
people = int(input("How many people to split the bill? "))

# Calculate the total tip amount
total_tip_amount = bill * (tip / 100)

# Calculate the final amount per person after rounding off to 2 decimal places
final_amount = round((bill + total_tip_amount) / people, 2)

# Print how much each person should pay
print(f"Each person should pay: ${final_amount}")
