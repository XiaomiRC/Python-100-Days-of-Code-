# Create a program using maths and f-Strings that tells us how many weeks we have left, if we live until 90 years old.
It will take your current age as the input and output a message with our time left in this format:
You have x weeks left.
Where x is replaced with the actual calculated number of weeks the input age has left until age 90.

```
# Take the age as input from the user
age = input()
#Convert the age into integer
age_as_int = int(age)

#Calculate the years left to live
years_left = 90 - age_as_int

#Calculate the weeks left to live assuming there are 52 weeks in a year
weeks_left = years_left * 52

#Use fprint to print the weeks_left without converting into str
print(f"You have {weeks_left} weeks left.")
```
