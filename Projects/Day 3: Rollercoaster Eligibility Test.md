# Write a program that can be used at the Rollercoaster Ticketing Counter to check if a person is eligible to ride the rollercoaster.
## Level 1
1. Only people who are 120 cms and above can ride the rollercoaster.
2. You need to take the height in cms as input from the person.

**NOTE** 
- You will find the flow chart in "Day 3: Rollercoaster 1 .pdf"

### Solution 1 
```
print("Welcome to the rollercoaster!")

# Take the height in cms as input
height = int(input("What is your height in cm?"))

# Use the if..else condition to determine eligibility to ride the rollercoaster
if height >= 120:
  print("You can ride the rollercoaster!")
else:
  print("Sorry, you have to grow taller before you can ride.")
```

## Level 2
3. You need to check if the person riding the rollercoaster needs a kid's ticket or an adult's ticket
4. If they are 18 years old or more, they need to pay $12.
5. If they are less than 18 years old, they need to pay $7.

**NOTE** 
- You will find the flow chart in "Day 3: Rollercoaster 2 .pdf"

### Solution 2
```
print("Welcome to the rollercoaster!")

# Take the height in cms as input
height = int(input("What is your height in cm?"))

# Use the if..else condition to determine eligibility to ride the rollercoaster
if height >= 120:
  print("You can ride the rollercoaster!")
  age = int(input("What is your age in years?"))
  if age >=18:
    print("Please pay $12.")
  else:
    print("Please pay $7.")
else:
  print("Sorry, you have to grow taller before you can ride.")
```
## Level 3
6. The amount that you need to pay according to your age has now been revised and the changed criteria is as follows:
7. If the age is more than 18 years old, you need to pay $12.
8. If the age is between 12 and 18 years old, you need to pay $7.
9. If they are less than 12 years old, you need to pay $5.

**NOTE** 
- You will find the flow chart in "Day 3: Rollercoaster 3 .pdf"

### Solution 3
```
print("Welcome to the rollercoaster!")

# Take the height in cms as input
height = int(input("What is your height in cm?"))

# Use the if..else condition to determine eligibility to ride the rollercoaster
if height >= 120:
  print("You can ride the rollercoaster!")
  age = int(input("What is your age in years?"))
  if age >18:
    print("Please pay $12.")
  elif age >=12:
    print("Please pay $7.")
  else:
    print("Please pay $5.")
else:
  print("Sorry, you have to grow taller before you can ride.")
```
