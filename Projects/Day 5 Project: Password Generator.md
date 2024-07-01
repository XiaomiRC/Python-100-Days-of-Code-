# Create a password generator
Which takes the number of letters, numbers and symbols you wish to have in your password and generates an output. It should work as shown below:

### Sample Run 1:
```css
Welcome to the PyPassword Generator!
How many letters would you like in your password?
2
How many symbols would you like?
2
How many numbers would you like?
2
Easy Level Password Generated: Ik(+96
Hard Level Password Generated: 9I(6k+
```

### Sample Run 2:
```css
Welcome to the PyPassword Generator!
How many letters would you like in your password?
2
How many symbols would you like?
2
How many numbers would you like?
2
Easy Level Password Generated: cb%!90
Hard Level Password Generated: %!b9c0
```
**NOTE**: In the above output, the Easy level has the letters, symbols and numbers together. We do not want to be that obvious which is why we generated the hard level password by shuffling it.

### My Solution:
```python
import random # Import the random module for generating random values

# Define lists of characters to use in password generation
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']  # List containing lowercase and uppercase letters
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']   # List containing numeric digits
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']        # List containing special symbols

print("Welcome to the PyPassword Generator!")   # Print a welcome message to the user

# Prompt the user for the number of each type of character to include in the password
nr_letters = int(input("How many letters would you like in your password?\n"))
nr_symbols = int(input("How many symbols would you like?\n"))
nr_numbers = int(input("How many numbers would you like?\n"))

# Generate random characters for the password based on user input
random_letters = random.sample(letters, nr_letters)    # Select nr_letters random letters
random_symbols = random.sample(symbols, nr_symbols)    # Select nr_symbols random symbols
random_numbers = random.sample(numbers, nr_numbers)    # Select nr_numbers random numbers

# Combine all randomly selected characters into a single list to form the password
password_list = random_letters + random_symbols + random_numbers
easy_password = ''.join(password_list)    # Convert the list of characters into a string to form the easy level password
print(f"Easy Level Password Generated: {easy_password}")

# Shuffle the password characters to make it random
random.shuffle(password_list)

# Convert the shuffled list of characters back into a string to form the hard level password
hard_password = ''.join(password_list)

print(f"Hard Level Password Generated: {hard_password}")
```
### Comments Explaining the Code:

#### Imports and Data Initialization:

- `import random`: Imports the random module for random number generation and shuffling.
- `letters`, `numbers`, `symbols`: Lists containing characters to be used in generating passwords.

#### User Input and Password Generation:

- `nr_letters`, `nr_symbols`, `nr_numbers`: Variables storing user input for the number of letters, symbols, and numbers in the password.
- `random.sample()`: Selects random elements from `letters`, `symbols`, and `numbers` lists based on user input.

#### Easy Level Password Generation:

- `password_list`: Combines randomly selected characters into a single list.
- `''.join(password_list)`: Converts the list of characters into a string (`easy_password`).

#### Hard Level Password Generation:

- `random.shuffle(password_list)`: Shuffles the `password_list` to randomize the order of characters.
- `''.join(password_list)`: Converts the shuffled list of characters into a string (`hard_password`).

#### Output:

- Prints the generated passwords for both easy and hard levels using formatted strings (`f"Easy Level Password Generated: {easy_password}"` and `f"Hard Level Password Generated: {hard_password}"`).

### Angela's Solution:
```python
import random  # Import the random module for random number generation and shuffling

# Define lists of characters to use in password generation
letters = ['a', 'b', 'c', ..., 'Z']  # List containing lowercase and uppercase letters
numbers = ['0', '1', '2', ..., '9']  # List containing numeric digits
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']  # List containing special symbols

print("Welcome to the PyPassword Generator!")  # Print a welcome message to the user

nr_letters = int(input("How many letters would you like in your password?\n"))  # Prompt user for number of letters in password
nr_symbols = int(input(f"How many symbols would you like?\n"))  # Prompt user for number of symbols in password
nr_numbers = int(input(f"How many numbers would you like?\n"))  # Prompt user for number of numbers in password

# Easy Level Password Generation
# password = ""
# for char in range(1, nr_letters + 1):
#   password += random.choice(letters)  # Append random letter to password

# for char in range(1, nr_symbols + 1):
#   password += random.choice(symbols)  # Append random symbol to password

# for char in range(1, nr_numbers + 1):
#   password += random.choice(numbers)  # Append random number to password

# print(password)  # Print the generated password

# Hard Level Password Generation
password_list = []

for char in range(1, nr_letters + 1):
  password_list.append(random.choice(letters))  # Append random letter to password_list

for char in range(1, nr_symbols + 1):
  password_list += random.choice(symbols)  # Extend password_list with random symbol

for char in range(1, nr_numbers + 1):
  password_list += random.choice(numbers)  # Extend password_list with random number

print(password_list)  # Print the list of characters before shuffling
random.shuffle(password_list)  # Shuffle the characters in password_list
print(password_list)  # Print the shuffled list of characters

# Convert password_list back to string format for the final password
password = ""
for char in password_list:
  password += char

print(f"Your password is: {password}")  # Print the final generated password

```
### Comments Explaining the Code:

#### Imports and Data Initialization:

- `import random`: Imports the random module for random number generation and shuffling.
- `letters`, `numbers`, `symbols`: Lists containing characters to be used in generating passwords.

#### Welcome Message and User Input:

- `print("Welcome to the PyPassword Generator!")`: Displays a welcome message to the user.
- `nr_letters`, `nr_symbols`, `nr_numbers`: Variables storing user input for the number of letters, symbols, and numbers in the password.

#### Easy Level Password Generation (Commented Out):

- The commented-out section (`#Easy Level`) shows an alternative approach to generating the password directly as a string using loops and `random.choice()`.

#### Hard Level Password Generation:

- `password_list`: Initializes an empty list to store characters for generating the password.
- Loops iterate to append or extend `password_list` with random characters from `letters`, `symbols`, and `numbers`.

#### Shuffling and Final Password:

- `random.shuffle(password_list)`: Shuffles the `password_list` to randomize the order of characters.
- Constructs the final password by iterating through `password_list` and concatenating characters into `password`.
- `print(f"Your password is: {password}")`: Displays the final generated password to the user.
