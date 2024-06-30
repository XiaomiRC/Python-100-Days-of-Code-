# Instructions

## Level 1
You are going to write a program that will select a random name from a list of names. The person selected will have to pay for everybody's food bill.

**Important**: You are not allowed to use the `choice()` function.

**Example Input:**
Angela, Ben, Jenny, Michael, Chloe

**Example Output:**
Michael is going to buy the meal today!

**Hints:**
You might need the help of the `len()` function. [Stack Overflow: How do I get the number of elements in a list?](https://stackoverflow.com/questions/1712227/how-do-i-get-the-number-of-elements-in-a-list)

Remember that Lists start at index 0!

### Solution 1 :

``` python
import random

# Example input from the problem statement
names = ["Angela", "Ben", "Jenny", "Michael", "Chloe"]

# Generate a random index within the range of the list `names`
random_index = random.randint(0, len(names) - 1)

# Retrieve the name at the randomly chosen index
selected_name = names[random_index]

# Print the output statement
print(f"{selected_name} is going to buy the meal today!")
```

## Level 2
**NOTE**: In this exercise, you are working collaboratively with another programmer. They already dealt with `input()` and writing the code needed to get hold of the names in the input area, so you don't need to worry about that.

The other programmer has written the code to separate the names in the input area into individual names and puts them inside a List called `names`. For their code to work correctly, you must enter all the names in the input area followed by a comma and a space. e.g. name, name, name

Assume that `names` works like this:

- input area: x, y, z,
- names = ["x", "y", "z"]


### Solution 2 :

```python
import random

# Get input from user
names_string = input("Enter the names separated by commas: ")

# Split the input string into a list of names
names = names_string.split(", ")

# Generate a random index within the range of the list `names`
random_index = random.randint(0, len(names) - 1)

# Retrieve the name at the randomly chosen index
selected_name = names[random_index]

# Print the output statement
print(f"{selected_name} is going to buy the meal today!")
```
