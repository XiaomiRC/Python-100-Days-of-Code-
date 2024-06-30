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

## Level 4
10. We're now providing the customer with photography services. The eligible customers can now opt for their photos being taken at $3 dollars. The bill needs to be modified to include the photo ticket in it


**NOTE** 
- You will find the flow chart in "Day 3: Rollercoaster 4 .pdf"

### Solution 4
```
print("Welcome to the rollercoaster!")

# Take the height in cms as input
height = int(input("What is your height in cm?"))

# Use the if..else condition to determine eligibility to ride the rollercoaster
if height >= 120:
  print("You can ride the rollercoaster!")
  bill=0  # declaring the variable bill
  age = int(input("What is your age in years?"))  # taking age as input
  if age >18:
    bill=12
    print("Adult tickets are $12.")
  elif age>=12:
    bill=7
    print("Youth tickers are $7.")
  else:
    bill=5
    print("Child tickets are $5.")

# Declare another variable photo to determine if the customer wants their photo taken
  photo = input(" Do you want a picture taken for $3?(y/n)")
  if photo == "y":
    # Add 3 dollars to the bill
    bill = bill + 3
    print(f"Your final bill is ${bill}")
  else:
    print(f"Your final bill is ${bill}")  # prints the bill without adding $3
else:
  print("Sorry, you have to grow taller before you can ride.")  # this is printed if the customer is less than 120 cms in height
```
## Level 5
11. We're now providing the customer udergoing mid-life crisis a free ride. As per wikipedia, mid-life crisis usually happens from 45 to 55 years of age. Modify the program to include this criteria.


**NOTE** 
- You will find the flow chart in "Day 3: Rollercoaster 5 .pdf"

### Solution 5
```
print("Welcome to the rollercoaster!")

# Take the height in cms as input
height = int(input("What is your height in cm?"))

# Use the if..else condition to determine eligibility to ride the rollercoaster
if height >= 120:
  print("You can ride the rollercoaster!")
  bill=0  # declaring the variable bill
  age = int(input("What is your age in years?"))  # taking age as input
  if age >=45 and age <=55:                       # using logical operators to find the group undergoing mid-life crisis. 
    print("Everything is going to be okay. Have a free ride on us!")
  elif age >18:
    bill=12
    print("Adult tickets are $12.")
  elif age>=12:
    bill=7
    print("Youth tickers are $7.")
  else:
    bill=5
    print("Child tickets are $5.")

# Declare another variable photo to determine if the customer wants their photo taken
  photo = input(" Do you want a picture taken for $3?(y/n)")
  if photo == "y":
    # Add 3 dollars to the bill
    bill = bill + 3
    print(f"Your final bill is ${bill}")
  else:
    print(f"Your final bill is ${bill}")  # prints the bill without adding $3
else:
  print("Sorry, you have to grow taller before you can ride.")  # this is printed if the customer is less than 120 cms in height
```
