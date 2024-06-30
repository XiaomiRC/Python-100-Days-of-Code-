# Write a program that can be used at the Rollercoaster Ticketing Counter to check if a person is eligible to ride the rollercoaster.
1. Only people who are 120 cms and above can ride the rollercoaster.
2. You need to take the height in cms as input from the person.

```
print("Welcome to the rollercoaster!")

# Take the height in cms as input
height = int(input("What is your height in cm?"))

# Use the if..else condition to determine eligibility to ride the rollercoaster
if height > 120:
  print("You can ride the rollercoaster!")
else:
  print("Sorry, you have to grow taller before you can ride.")
```
