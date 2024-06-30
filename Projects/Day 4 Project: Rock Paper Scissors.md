# Question:
You are tasked with developing a Python program to simulate a game of Rock, Paper, Scissors against the computer. The game involves choosing between three options: Rock, Paper, or Scissors. Based on your choice and a random selection made by the computer, different outcomes determine the winner. Write a Python program that implements this game and prints the result based on the user's input.

### Requirements:
- **Input**: Prompt the user to enter their choice (0 for Rock, 1 for Paper, 2 for Scissors).
- **Output**: Display the user's choice, the computer's choice, and the result (Win, Lose, or Draw).
- **Logic**: Use conditional statements to determine the winner based on the game rules:
  - Rock beats Scissors
  - Scissors beats Paper
  - Paper beats Rock
  - A draw occurs when both choose the same option.

### Constraints:
- Ensure the program handles invalid inputs gracefully (e.g., inputs other than 0, 1, or 2).
- Use appropriate data structures and control flow to simulate the game effectively.

### Solution 1:
```python
import random

rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

index = [rock, paper, scissors]

user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors:\n "))
random_choice = random.randint(0, 2)

if user_choice == 0 and random_choice == 0:
    print(f"You chose {index[user_choice]}")
    print(f"I chose {index[random_choice]}")
    print("It's a draw")
elif user_choice == 0 and random_choice == 1:
    print(f"You chose {index[user_choice]}")
    print(f"I chose {index[random_choice]}")
    print("You lose")
elif user_choice == 0 and random_choice == 2:
    print(f"You chose {index[user_choice]}")
    print(f"I chose {index[random_choice]}")
    print("You win")
elif user_choice == 1 and random_choice == 0:
    print(f"You chose {index[user_choice]}")
    print(f"I chose {index[random_choice]}")
    print("You win")
elif user_choice == 1 and random_choice == 1:
    print(f"You chose {index[user_choice]}")
    print(f"I chose {index[random_choice]}")
    print("It's a draw")
elif user_choice == 1 and random_choice == 2:
    print(f"You chose {index[user_choice]}")
    print(f"I chose {index[random_choice]}")
    print("You lose")
elif user_choice == 2 and random_choice == 0:
    print(f"You chose {index[user_choice]}")
    print(f"I chose {index[random_choice]}")
    print("You lose")
elif user_choice == 2 and random_choice == 1:
    print(f"You chose {index[user_choice]}")
    print(f"I chose {index[random_choice]}")
    print("You win")
elif user_choice == 2 and random_choice == 2:
    print(f"You chose {index[user_choice]}")
    print(f"I chose {index[random_choice]}")
    print("It's a draw")
```
### Solution 2:
```python
import random

# Multiline strings for rock, paper, and scissors
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

# List of options
index = [rock, paper, scissors]

# User input for choice
user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper, or 2 for Scissors:\n"))

# Validate user input
if user_choice not in [0, 1, 2]:
    print("Invalid choice. Please choose 0 for Rock, 1 for Paper, or 2 for Scissors.")
else:
    # Generate random choice for computer
    random_choice = random.randint(0, 2)

    # Print user and computer choices
    print(f"You chose:\n{index[user_choice]}")
    print(f"I chose:\n{index[random_choice]}")

    # Determine the result based on choices
    if user_choice == random_choice:
        print("It's a draw!")
    elif (user_choice == 0 and random_choice == 2) or \
         (user_choice == 1 and random_choice == 0) or \
         (user_choice == 2 and random_choice == 1):
        print("You win!")
    else:
        print("You lose!")
```
