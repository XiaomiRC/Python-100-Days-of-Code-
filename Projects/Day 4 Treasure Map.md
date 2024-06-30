# Instructions

This is a difficult challenge. 💪

You are going to write a program that will mark a spot on a map with an X.

In the starting code, you will find a variable called `map`.

This map contains a nested list. When `map` is printed, this is what it looks like, notice the nesting:
```
[['⬜️', '⬜️', '⬜️'],
['⬜️', '⬜️', '⬜️'],
['⬜️', '⬜️', '⬜️']]
```
This is a bit hard to work with. So on lines 6 and 23, we've used this line of code `print(f"{line1}\n{line2}\n{line3}")` to format the 3 lists to be printed as a 3 by 3 grid, each on a new line.
```
['⬜️', '⬜️', '⬜️']
['⬜️', '⬜️', '⬜️']
['⬜️', '⬜️', '⬜️']
```
Now it looks a bit more like the coordinates of a real map:

Your job is to write a program that allows you to mark a square on the map using a letter-number system.

So an input of `A3` should place an X at the position shown below:
  ```
       A     B     C 
1 ['⬜️', '⬜️', '⬜️']
2 ['⬜️', '⬜️', '⬜️']
3 ['⬜️', 'X ', '⬜️']
```

### Example Input 1
B3
### Example Output 1
Hiding your treasure! X marks the spot.
```
['⬜️', '️⬜️', '️⬜️']
['⬜️', '⬜️', '️⬜️']
['⬜️️', 'X', '⬜️️']
```

### Example Input 2
B1
### Example Output 2
Hiding your treasure! X marks the spot.
```
['⬜️', 'X',  '️⬜️']
['⬜️', '⬜️', '️⬜️']
['⬜️️', '⬜️️', '⬜️️']
```
### Hints
- See if this [List method](https://www.w3schools.com/python/ref_list_index.asp) helps you.
- Remember that nested Lists in Python are accessed from outside to inside. e.g. In the List below:

list = [['A', 'B', 'C'], 'E', 'F', 'G']
E is list[1]
C is list[0][2]

- Check your formatting. This is correctly formatted:
```
['⬜️', '⬜️', '⬜️']
['⬜️', '⬜️', '⬜️']
['⬜️', 'X',  '⬜️']
```
vs.
Incorrectly formatted (missing a space before 'X' and extra space after the 'X' and extra space before the comma):
```
['⬜️', '⬜️', '⬜️']
['⬜️', '⬜️', '⬜️']
['⬜️', 'X ' , '⬜️']
```
### Solution:
```python
line1 = ["⬜️","️⬜️","️⬜️"]
line2 = ["⬜️","⬜️","️⬜️"]
line3 = ["⬜️️","⬜️️","⬜️️"]
treasure_map = [line1, line2, line3]

print("Hiding your treasure! X marks the spot.")
position = input("Where do you want to put the treasure? (e.g., A1): ").upper()  # Ensure input is in uppercase

# Validate position input (assuming a basic check for simplicity)
if len(position) != 2 or position[0] not in "ABC" or position[1] not in "123":
    print("Invalid position! Please provide a position like A1, B2, C3.")
else:
    letter = position[0]  # Extract letter part
    number = int(position[1])  # Extract number part

    # Convert letter to index
    abc = ["A", "B", "C"]
    letter_index = abc.index(letter)

    # Adjust index for Python list (starting from 0)
    number_index = number - 1

    # Place the treasure "X" on the map
    treasure_map[number_index][letter_index] = "X"

    # Print the updated treasure map
    print(f"{treasure_map[0]}\n{treasure_map[1]}\n{treasure_map[2]}")
```
