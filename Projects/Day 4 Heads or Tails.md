### Question:

You are tasked with writing a Python program to simulate a coin toss using the `random` module. Write the code that generates either "Heads" or "Tails" randomly based on the outcome of the coin toss.

### Explanation:

To simulate a coin toss in Python, we can use the `random.randint()` function from the `random` module. Here's a breakdown of how the provided code accomplishes this:

1. **Importing the random module:**
   - `import random` imports the `random` module in Python, which provides functions for generating random numbers.

2. **Generating a random integer:**
   - `random.randint(0, 1)` generates a random integer that can be either 0 or 1.

3. **Conditional statement:**
   - The `if` statement checks if the randomly generated integer (`random_int`) equals 0 (`random_int == 0`).
   - If true, it prints `"Tails"`.
   - Otherwise (if `random_int` is 1), it prints `"Heads"`.

### Python Code:

```python
import random

# Generate a random integer (0 or 1) to simulate a coin toss
random_int = random.randint(0, 1)

# Determine the outcome of the coin toss and print the result
if random_int == 0:
    print("Tails")
else:
    print("Heads")
