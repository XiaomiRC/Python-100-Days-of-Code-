### Question:

Create a program for a Rollercoaster Ticketing Counter that determines eligibility based on height and age, calculates the ticket cost, and optionally includes a photography service charge.

### Level 1

1. Only people who are 120 cm and above can ride the rollercoaster.
2. Take the height in cm as input from the person.

### Solution 1

```python
print("Welcome to the rollercoaster!")

# Take the height in cm as input
height = int(input("What is your height in cm?"))

# Use an if..else condition to determine eligibility to ride the rollercoaster
if height >= 120:
  print("You can ride the rollercoaster!")
else:
  print("Sorry, you have to grow taller before you can ride.")
```

## Level 2
3. Determine if the person needs a kid's ticket or an adult's ticket:
- If 18 years or older, pay $12.
- If younger than 18 years, pay $7.

**NOTE** 
- You will find the flow chart in "Day 3: Rollercoaster 2 .pdf"

### Solution 2

``` python
print("Welcome to the rollercoaster!")

# Take the height in cm as input
height = int(input("What is your height in cm?"))

# Use an if..else condition to determine eligibility to ride the rollercoaster
if height >= 120:
  print("You can ride the rollercoaster!")
  
  # Ask for age to determine ticket price
  age = int(input("What is your age in years?"))
  if age >= 18:
    print("Please pay $12.")
  else:
    print("Please pay $7.")
else:
  print("Sorry, you have to grow taller before you can ride.")
```

## Level 3
4. Revise the ticket cost based on age:
- Age > 18 years: $12
- Age between 12 and 18 years: $7
- Age < 12 years: $5

**NOTE** 
- You will find the flow chart in "Day 3: Rollercoaster 3 .pdf"

### Solution 3
``` python
print("Welcome to the rollercoaster!")

# Take the height in cm as input
height = int(input("What is your height in cm?"))

# Use an if..else condition to determine eligibility to ride the rollercoaster
if height >= 120:
  print("You can ride the rollercoaster!")
  
  # Ask for age to determine ticket price
  age = int(input("What is your age in years?"))
  if age > 18:
    print("Please pay $12.")
  elif age >= 12:
    print("Please pay $7.")
  else:
    print("Please pay $5.")
else:
  print("Sorry, you have to grow taller before you can ride.")

```

## Level 4
5. Offer photography services at $3:
- Include this in the final bill calculation.

**NOTE** 
- You will find the flow chart in "Day 3: Rollercoaster 4 .pdf"

### Solution 4
```python
print("Welcome to the rollercoaster!")

# Take the height in cm as input
height = int(input("What is your height in cm?"))

# Use an if..else condition to determine eligibility to ride the rollercoaster
if height >= 120:
  print("You can ride the rollercoaster!")
  
  # Initialize bill variable
  bill = 0
  
  # Ask for age to determine ticket price
  age = int(input("What is your age in years?"))
  if age >= 45 and age <= 55:
    print("Everything is going to be okay. Have a free ride on us!")
  elif age > 18:
    bill = 12
    print("Adult tickets are $12.")
  elif age >= 12:
    bill = 7
    print("Youth tickets are $7.")
  else:
    bill = 5
    print("Child tickets are $5.")
  
  # Ask if they want a photo taken
  photo = input("Do you want a picture taken for $3? (y/n)")
  if photo == "y":
    bill += 3
  
  print(f"Your final bill is ${bill}")
else:
  print("Sorry, you have to grow taller before you can ride.")

```
## Level 5
6. Offer a free ride to individuals experiencing a mid-life crisis, ages 45 to 55.

**NOTE** 
- You will find the flow chart in "Day 3: Rollercoaster 5 .pdf"

### Solution 5
```python
print("Welcome to the rollercoaster!")

# Take the height in cm as input
height = int(input("What is your height in cm?"))

# Use an if..else condition to determine eligibility to ride the rollercoaster
if height >= 120:
  print("You can ride the rollercoaster!")
  
  # Initialize bill variable
  bill = 0
  
  # Ask for age to determine ticket price
  age = int(input("What is your age in years?"))
  if age >= 45 and age <= 55:
    print("Everything is going to be okay. Have a free ride on us!")
  elif age > 18:
    bill = 12
    print("Adult tickets are $12.")
  elif age >= 12:
    bill = 7
    print("Youth tickets are $7.")
  else:
    bill = 5
    print("Child tickets are $5.")
  
  # Ask if they want a photo taken
  photo = input("Do you want a picture taken for $3? (y/n)")
  if photo == "y":
    bill += 3
  
  print(f"Your final bill is ${bill}")
else:
  print("Sorry, you have to grow taller before you can ride.")

```
