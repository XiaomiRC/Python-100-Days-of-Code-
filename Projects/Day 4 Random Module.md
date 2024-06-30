### Question:

You have a Python program that generates two random numbers:

- `random_int`: an integer between 1 and 10 (inclusive).
- `random_float`: a float between 0 and 1 (exclusive).

Additionally, the program calculates a scaled value of `random_float` by multiplying it by 5.

Finally, it generates a `love_score`, which is a random integer between 1 and 100.

Write a Python program that replicates this behavior and prints out the values of `random_int`, `random_float` (rounded to 3 decimal places), `scaled_float` (rounded to 3 decimal places), and the `love_score`.

### Steps to Solve:

1. **Import the random module:**
   - Use the `import random` statement to import the necessary module for generating random numbers.

2. **Generate `random_int`:**
   - Use `random.randint(1, 10)` to generate a random integer between 1 and 10 (inclusive).

3. **Generate `random_float`:**
   - Use `random.random()` to generate a random float between 0 and 1 (exclusive).

4. **Calculate `scaled_float`:**
   - Multiply `random_float` by 5 to get a scaled value.

5. **Generate `love_score`:**
   - Use `random.randint(1, 100)` to generate a random integer between 1 and 100.

6. **Print the results:**
   - Print `random_int`, `random_float` (rounded to 3 decimal places), `scaled_float` (rounded to 3 decimal places), and `love_score` in a formatted string.

### Solution

```
import random

random_int = random.randint(1, 10)  # Generate a random integer between 1 and 10
print(random_int)

random_float = random.random()  # Generate a random float between 0 and 1
print(random_float)

scaled_float = random_float * 5  # Multiply the random float by 5
print(scaled_float)

love_score = random.randint(1, 100)  # Generate a random integer between 1 and 100
print(f"Your love score is {love_score}")  # Print the love score
```
