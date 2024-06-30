# Treasure Island Adventure

You find yourself standing on a cliff overlooking a vast ocean, with a small island visible in the distance. Legend has it that this island holds a long-lost treasure that many have sought but none have found. Determined to be the one who uncovers its secrets, you decide to embark on an adventure.

## Scene 1: The Crossroad

You're standing at a crossroad deep within a dense forest. The path splits into two: one leading left and the other right. You hear whispers of ancient tales suggesting that the left path might lead you closer to the treasure.

- **Choice 1:** Do you go **left** or **right**?

## Scene 2: The Lake

You follow the left path and soon arrive at the edge of a tranquil lake. The island with the treasure glimmers in the center of the lake, teasing you with its secrets. How will you proceed?

- **Choice 2:** Do you **wait** patiently for a boat or **swim** across the lake?

## Scene 3: The Island

You reach the island safely, greeted by a mysterious house with three doors: one red, one yellow, and one blue. Each door holds its own challenges and rewards.

- **Choice 3:** Which door will you choose to open? **Red**, **yellow**, or **blue**?

  - **Red Door:** You enter a room engulfed in flames, a fiery inferno that consumes everything. **Game Over.**
  
  - **Yellow Door:** Congratulations! You discover the hidden treasure, surrounded by gold and jewels. **You Win!**
  
  - **Blue Door:** You step into a room filled with wild beasts, their eyes glowing with hunger. **Game Over.**
  
  - **Any other choice:** You stumble into an invisible trap and are lost forever in the depths of the house. **Game Over.**

This Treasure Island adventure takes you through thrilling challenges and unexpected twists. Your fate lies in every decision you make. Are you ready to uncover the treasure and become the legendary treasure hunter?

**NOTE**
The flowchart for this game is in "Projects/Day 3 Project: Treasure+Island+Flowchart.pdf" file

### Solution

```
print("Welcome to Treasure Island!")
print("You find yourself at a crossroad in a dense forest.")
print("Legend has it that a treasure awaits on a mysterious island.")

# Scene 1: The Crossroad
choice1 = input('Where do you want to go? Type "left" or "right": ').lower()

if choice1 == "left":
    # Scene 2: The Lake
    choice2 = input('You\'ve come to a lake. There is an island in the middle of the lake. '
                    'Type "wait" to wait for a boat. Type "swim" to swim across: ').lower()

    if choice2 == "wait":
        # Scene 3: The Island
        choice3 = input("You arrive at the island unharmed. There is a house with 3 doors. "
                        "One red, one yellow, and one blue. Which colour do you choose? ").lower()

        if choice3 == "red":
            print("It's a room full of fire. Game Over.")
        elif choice3 == "yellow":
            print("Congratulations! You found the treasure! You Win!")
        elif choice3 == "blue":
            print("You enter a room of beasts. Game Over.")
        else:
            print("You chose a door that doesn't exist. Game Over.")

    else:
        print("You get attacked by an angry trout. Game Over.")

else:
    print("You fell into a hole. Game Over.")
```

