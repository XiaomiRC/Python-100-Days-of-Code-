# Instructions
You are going to write a program that calculates the sum of all the even numbers from 1 to X. If X is 100 then the first even number would be 2 and the last one is 100:

### Example Calculation:
```
2 + 4 + 6 + 8 + ... + 98 + 100
```
**Important:** There should only be 1 print statement in your console output. It should just print the final total and not every step of the calculation.

**Constraints:** Inputs are constrained to numbers from 0 to a maximum of 1000.

### Example Input 1
```
10
```
### Example Output 1
```
30
```
### Example Input 2
```
52
```
### Example Output 2
```
702
```
### Hint:
There are quite a few ways of solving this problem, but you will need to use the `range()` function in any of the solutions.

### Solution:

```python
target = int(input("Enter a number between 0 and 1000"))  # Enter a number between 0 and 1000

total = 0  # Initialize total to accumulate the sum of even numbers

# Check if the input number (target) is within the range of 0 to 1000
if target >= 0 and target <= 1000:
    # Iterate through even numbers from 0 up to and including the target
    # with a step of 2 (i.e., 0, 2, 4, ..., up to target)
    for even in range(0, target + 1, 2):
        total += even  # Add each even number to the total sum
else:
  print("Invalid input")

# Print the total sum of even numbers up to and including the target
print(total)

```
