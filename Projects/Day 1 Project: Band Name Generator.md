# Day 1 Project: Band Name Generator
### Question:

You are creating a Python program that generates a band name based on user input:

- Prompt the user with a welcoming message: `"Welcome to the Band Name Generator"`.
- Ask the user for the name of the city they grew up in.
- Ask the user for their pet's name.
- Combine the city and pet names to generate a band name.
- Print the generated band name.

Write a Python program that accomplishes this task.

### Steps to Solve:

1. **Print a welcoming message:**
   - Use `print("Welcome to the Band Name Generator")` to display a greeting to the user.

2. **Input the city name:**
   - Use `input("What's the name of the city you grew up in?\n")` to prompt the user to enter the name of the city they grew up in.
   - Store the user's input in a variable, e.g., `city`.

3. **Input the pet's name:**
   - Use `input("What's your pet's name?\n")` to prompt the user to enter their pet's name.
   - Store the user's input in a variable, e.g., `pet`.

4. **Generate the band name:**
   - Concatenate the `city` and `pet` variables to form the band name string, e.g., `band_name = city + " " + pet`.

5. **Print the band name:**
   - Use `print("Your band name could be " + band_name)` to display the generated band name to the user.

### Python Code:

```python
print("Welcome to the Band Name Generator")
city = input("What's the name of the city you grew up in?\n")
pet = input("What's your pet's name?\n")
band_name = city + " " + pet
print("Your band name could be " + band_name)

