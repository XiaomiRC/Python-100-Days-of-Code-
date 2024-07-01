# Congratulations, you've got a job at Python Pizza! Your first job is to build an automatic pizza order program.

Based on a user's order, work out their final bill.

Small pizza (S): $15

Medium pizza (M): $20

Large pizza (L): $25

Add pepperoni for small pizza (Y or N): +$2

Add pepperoni for medium or large pizza (Y or N): +$3

Add extra cheese for any size pizza (Y or N): +$1

### Example Input
- L
- Y
- N

### Example Output
- Thank you for choosing Python Pizza Deliveries!
- Your final bill is: $28.

```python
# Display a welcome message to the user
print("Thank you for choosing Python Pizza Deliveries!\n")

# Ask the user for the size of the pizza
size = input("What size pizza do you want? S, M, or L\n") 

# Ask the user if they want pepperoni
add_pepperoni = input("Do you want pepperoni? Y or N\n")

# Ask the user if they want extra cheese
extra_cheese = input("Do you want extra cheese? Y or N\n") 

# Initialize the variable "bill" to 0
bill = 0

# Assigning the base price of the pizza based on its size
if size == "S":
    bill = 15
elif size == "M":
    bill = 20
else:
    bill = 25

# Adding the charge for pepperoni based on the size of the pizza
if add_pepperoni == "Y":
    if size == "S":
        bill += 2
    else:
        bill += 3

# Adding the charge for extra cheese to the bill
if extra_cheese == "Y":
    bill += 1

# Print the final bill to the user
print(f"Your final bill is: ${bill}.")

```
