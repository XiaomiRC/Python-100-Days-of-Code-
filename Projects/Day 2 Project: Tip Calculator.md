# Create a Tip Calculator which will calculate the tip you need to pay in case you are going out to eat at a restaurant with your friends.
## What the Calculator should do?
1. If the bill was $150.00, split between 5 people, with 12% tip. 
2. Each person should pay (150.00 / 5) * 1.12 = 33.6
3. Round the result to 2 decimal places.

```
print("Welcome to the tip calculator!")

# Ask the user to provide the total bill amount, the percentage of tip they wish to provide and the number of people who will be splitting the bill
bill = float(input("What was the total bill? $"))
tip = int(input("How much percent of the bill would you like to give as tip? 10, 12, or 15? "))
people = int(input("How many people to split the bill? "))

# Calculate the total tip amount using the tip percent mentioned in the input above. 
total_tip_amount =  bill * (tip / 100)

# Divide the total bill and the tip amount among the number of people after rounding off to 2 decimal places.
final_amount = round((bill + total_tip_amount) / people,2)

# Print how much each person should pay 
print(f"Each person should pay: ${final_amount}")
```
