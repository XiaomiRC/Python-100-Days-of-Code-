# Write a program that works out whether if a given year is a leap year. 

A normal year has 365 days, leap years have 366, with an extra day in February. The reason why we have leap years is really fascinating, this video does it more justice. This is how you work out whether if a particular year is a leap year.
A leap year is:
    - Divisible by 4
    - Not divisible by 100, unless divisible by 400

**NOTE**
- Try using this flow chart in "Day 3: Leap Year Algorithm.pdf".

e.g. The year 2000:

2000 ÷ 4 = 500 (Leap)

2000 ÷ 100 = 20 (Not Leap)

2000 ÷ 400 = 5 (Leap!)

So the year 2000 is a leap year.

But the year 2100 is not a leap year because:

2100 ÷ 4 = 525 (Leap)

2100 ÷ 100 = 21 (Not Leap)

2100 ÷ 400 = 5.25 (Not Leap)

### Example Input 1
2400
### Example Output 1
Leap year
### Example Input 2
1989
### Example Output 2
Not leap year

### Solution
```
# Ask user to input the year they wish to check 
print("This is the Leap Year Checker!")
year = int(input("Which year do you want to check?"))

# if the year is divisible by 4, 100 and 400 without remainder, it is a leap year.
# if the year is divisible by 4 and 100 but not by 400, it is not a leap year.
# if the year is divisible by 4 and not by 100, it is a leap year.
# if the year is not divisible by 4, it is not a leap year.
if year % 4 == 0:
  if year % 100 == 0:
    if year % 400 == 0:
      print("Leap year")
    else:
      print("Not leap year")
  else:
    print("Leap year")
else:
  print("Not leap year")

 ```
