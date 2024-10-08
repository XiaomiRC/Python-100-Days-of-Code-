# Instructions

You are going to write a program that automatically prints the solution to the FizzBuzz game. These are the rules of the FizzBuzz game:

1. Your program should print each number from 1 to 100 in turn and include number 100.

2. When the number is divisible by 3, then instead of printing the number it should print "Fizz".

3. When the number is divisible by 5, then instead of printing the number it should print "Buzz".

4. If the number is divisible by both 3 and 5 (e.g., 15), then instead of the number it should print "FizzBuzz".

### Example Output:
```css
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
...etc (up to 100)
```
### Hint:
Remember your answer should start from 1 and go up to and including 100.

Each number/text should be printed on a separate line.

### Solution:
```python
# Loop through numbers from 1 to 100 (inclusive)
for num in range(1, 100+1):
    # Check if the number is divisible by both 3 and 5
    if num % 3 == 0 and num % 5 == 0:
        print("FizzBuzz")
    # Check if the number is divisible by 3 only
    elif num % 3 == 0:
        print("Fizz")
    # Check if the number is divisible by 5 only
    elif num % 5 == 0:
        print("Buzz")
    # If none of the above conditions are true, print the
```
