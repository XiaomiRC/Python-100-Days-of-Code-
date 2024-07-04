# Question: 
You are developing a Hangman game in Python. The game randomly selects a word from a predefined list, and the player has a limited number of attempts to guess the letters in the word. Each incorrect guess results in the display of a part of the hangman. The game ends when the player correctly guesses all the letters in the word or runs out of attempts.
- Use `hangman_art.py` to import logos and hangman stages 
- Use `hangman_words.py` to import the `word_list`
- Use `Day 7 Hangman Flowchart - 1.png` to build the easier version
- Use `Day 7 Amended Hangman Flowchart - 1.png` to build the easier version

**Hint 1** - Selecting a Random Word from a List of Words 
```python
import random

# List of words to choose from
word_list = ["ardvark", "baboon", "camel", "python", "programming", "hangman"]

# Select a random word from the list
chosen_word = random.choice(word_list)
```
**Hint 2** -Initializing the Display to Show Blanks for Each Letter in the Word
```python
# Determine the length of the chosen word
word_length = len(chosen_word)

# Initialize display_blanks with underscores for each letter in the word
display_blanks = ["_"] * word_length
```
**Hint 3** -Accepting and Validating User Input for Guesses
```python
# Accept user input for a letter guess, and validate it
guess = input("Guess a letter: ").lower()

# Validate the input (check if it's a single letter and if it hasn't been guessed before)
while len(guess) != 1 or not guess.isalpha():
    print("Please enter a single letter.")
    guess = input("Guess a letter: ").lower()
```
**Hint 4** - Updating the Display to Reveal Correctly Guessed Letters
```python
# Iterate through the chosen word to check for the guessed letter
for index, letter in enumerate(chosen_word):
    if letter == guess:
        display_blanks[index] = letter
```
**Hint 5** - Decrementing Attempts (Lives) on Incorrect Guesses
```python
# Check if the guessed letter is not in the chosen word
if guess not in chosen_word:
    life -= 1
    print("Incorrect guess. You lose a life.")
```
**Hint 6** - Determining and Displaying the Outcome of the Game (Win or Lose)
```python
# Check if all letters have been guessed correctly
if "_" not in display_blanks:
    print("Congratulations! You guessed the word:", chosen_word)
else:
    print("You ran out of lives. The word was:", chosen_word)
```
How you would initialize the display to show blanks for each letter in the word.
The process of accepting and validating user input for guesses.
How you would update the display to reveal correctly guessed letters.
The mechanism for decrementing attempts (lives) on incorrect guesses.
How you would determine and display the outcome of the game (win or lose).

### Code For Testing Purpose:
[Note] This has a few extra variables
```python
import random

# Importing the logo and displaying it
from hangman_art import logo
print(logo)

# Importing the list of words for the game
from hangman_words import word_list

# Choosing a random word from word_list
chosen_word = random.choice(word_list)
print(f"The solution is {chosen_word}")

# Determining the length of the chosen word
word_length = len(chosen_word)

# Setting initial number of lives
life = 6

# Initializing list to display blanks for each letter in the chosen word
display_blanks = ["_"] * word_length
print(display_blanks)

# Main game loop: continues while there are lives left and blanks to fill
while life > 0 and "_" in display_blanks:
    guess = input("Guess a letter: ").lower()  # Prompting user to guess a letter and converting to lowercase
    found = False  # Flag to track if the guessed letter is found in the chosen word
    
    if guess in display_blanks:
        print(f"You've already guessed {guess}")  # Informing the user if the letter has already been guessed
    
    # Iterating through each position in the chosen word
    for position in range(word_length):
        letter = chosen_word[position]
        
        if letter == guess:
            display_blanks[position] = letter  # Replacing underscore with the correctly guessed letter
            found = True  # Setting found to True if the letter is found in the chosen word
    
    # If the guessed letter is not found in the chosen word
    if not found:
        life -= 1  # Deducting a life
        print("You guessed a letter that's not in the word. You lose a life.")
        
        # Importing and displaying the appropriate hangman stage
        from hangman_art import stages
        print(stages[life])
    
    # Printing current life count and display of guessed and remaining letters
    print("life =", life)
    print(display_blanks)

# After exiting the loop, check if player has run out of lives or successfully guessed the word
if life == 0:
    print("You lose. The word was:", chosen_word)
else:
    print("Congratulations! You guessed the word:", chosen_word)
```

### My Solution:
#### 1. main.py:
```python
import random

# Importing the logo and displaying it
from hangman_art import logo
print(logo)

# Importing the list of words for the game
from hangman_words import word_list

# Choosing a random word from word_list
chosen_word = random.choice(word_list)

# Determining the length of the chosen word
word_length = len(chosen_word)

# Setting initial number of lives
life = 6

# Initializing list to display blanks for each letter in the chosen word
display_blanks = ["_"] * word_length
print(display_blanks)

# Main game loop: continues while there are lives left and blanks to fill
while life > 0 and "_" in display_blanks:
    guess = input("Guess a letter: ").lower()  # Prompting user to guess a letter and converting to lowercase
    found = False  # Flag to track if the guessed letter is found in the chosen word
    
    if guess in display_blanks:
        print(f"You've already guessed {guess}")  # Informing the user if the letter has already been guessed
    
    # Iterating through each position in the chosen word
    for position in range(word_length):
        letter = chosen_word[position]
        
        if letter == guess:
            display_blanks[position] = letter  # Replacing underscore with the correctly guessed letter
            found = True  # Setting found to True if the letter is found in the chosen word
    
    # If the guessed letter is not found in the chosen word
    if not found:
        life -= 1  # Deducting a life
        print("You guessed a letter that's not in the word. You lose a life.")
        
        # Importing and displaying the appropriate hangman stage
        from hangman_art import stages
        print(stages[life])
    
    # Printing display of guessed and remaining letters
    
    print(display_blanks)

# After exiting the loop, check if player has run out of lives or successfully guessed the word
if life == 0:
    print("You lose. The word was:", chosen_word)
else:
    print("Congratulations! You guessed the word:", chosen_word)
```
#### 2. hangman_art.py:
```python
stages = ['''
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
 /    |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|   |
      |
      |
=========''', '''
  +---+
  |   |
  O   |
  |   |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
      |
      |
      |
=========
''', '''
  +---+
  |   |
      |
      |
      |
      |
=========
''']

logo = ''' 
 _                                             
| |                                            
| |__   __ _ _ __   __ _ _ __ ___   __ _ _ __  
| '_ \ / _` | '_ \ / _` | '_ ` _ \ / _` | '_ \ 
| | | | (_| | | | | (_| | | | | | | (_| | | | |
|_| |_|\__,_|_| |_|\__, |_| |_| |_|\__,_|_| |_|
                    __/ |                      
                   |___/    '''


```
#### 3. hangman_words.py
```python
word_list = [
'abruptly', 
'absurd', 
'abyss', 
'affix', 
'askew', 
'avenue', 
'awkward', 
'axiom', 
'azure', 
'bagpipes', 
'bandwagon', 
'banjo', 
'bayou', 
'beekeeper', 
'bikini', 
'blitz', 
'blizzard', 
'boggle', 
'bookworm', 
'boxcar', 
'boxful', 
'buckaroo', 
'buffalo', 
'buffoon', 
'buxom', 
'buzzard', 
'buzzing', 
'buzzwords', 
'caliph', 
'cobweb', 
'cockiness', 
'croquet', 
'crypt', 
'curacao', 
'cycle', 
'daiquiri', 
'dirndl', 
'disavow', 
'dizzying', 
'duplex', 
'dwarves', 
'embezzle', 
'equip', 
'espionage', 
'euouae', 
'exodus', 
'faking', 
'fishhook', 
'fixable', 
'fjord', 
'flapjack', 
'flopping', 
'fluffiness', 
'flyby', 
'foxglove', 
'frazzled', 
'frizzled', 
'fuchsia', 
'funny', 
'gabby', 
'galaxy', 
'galvanize', 
'gazebo', 
'giaour', 
'gizmo', 
'glowworm', 
'glyph', 
'gnarly', 
'gnostic', 
'gossip', 
'grogginess', 
'haiku', 
'haphazard', 
'hyphen', 
'iatrogenic', 
'icebox', 
'injury', 
'ivory', 
'ivy', 
'jackpot', 
'jaundice', 
'jawbreaker', 
'jaywalk', 
'jazziest', 
'jazzy', 
'jelly', 
'jigsaw', 
'jinx', 
'jiujitsu', 
'jockey', 
'jogging', 
'joking', 
'jovial', 
'joyful', 
'juicy', 
'jukebox', 
'jumbo', 
'kayak', 
'kazoo', 
'keyhole', 
'khaki', 
'kilobyte', 
'kiosk', 
'kitsch', 
'kiwifruit', 
'klutz', 
'knapsack', 
'larynx', 
'lengths', 
'lucky', 
'luxury', 
'lymph', 
'marquis', 
'matrix', 
'megahertz', 
'microwave', 
'mnemonic', 
'mystify', 
'naphtha', 
'nightclub', 
'nowadays', 
'numbskull', 
'nymph', 
'onyx', 
'ovary', 
'oxidize', 
'oxygen', 
'pajama', 
'peekaboo', 
'phlegm', 
'pixel', 
'pizazz', 
'pneumonia', 
'polka', 
'pshaw', 
'psyche', 
'puppy', 
'puzzling', 
'quartz', 
'queue', 
'quips', 
'quixotic', 
'quiz', 
'quizzes', 
'quorum', 
'razzmatazz', 
'rhubarb', 
'rhythm', 
'rickshaw', 
'schnapps', 
'scratch', 
'shiv', 
'snazzy', 
'sphinx', 
'spritz', 
'squawk', 
'staff', 
'strength', 
'strengths', 
'stretch', 
'stronghold', 
'stymied', 
'subway', 
'swivel', 
'syndrome', 
'thriftless', 
'thumbscrew', 
'topaz', 
'transcript', 
'transgress', 
'transplant', 
'triphthong', 
'twelfth', 
'twelfths', 
'unknown', 
'unworthy', 
'unzip', 
'uptown', 
'vaporize', 
'vixen', 
'vodka', 
'voodoo', 
'vortex', 
'voyeurism', 
'walkway', 
'waltz', 
'wave', 
'wavy', 
'waxy', 
'wellspring', 
'wheezy', 
'whiskey', 
'whizzing', 
'whomever', 
'wimpy', 
'witchcraft', 
'wizard', 
'woozy', 
'wristwatch', 
'wyvern', 
'xylophone', 
'yachtsman', 
'yippee', 
'yoked', 
'youthful', 
'yummy', 
'zephyr', 
'zigzag', 
'zigzagging', 
'zilch', 
'zipper', 
'zodiac', 
'zombie', 
]
```
### 100 Days of Python Solution:
```python
#Step 5

import random

#TODO-1: - Update the word list to use the 'word_list' from hangman_words.py
#Delete this line: word_list = ["ardvark", "baboon", "camel"]
from hangman_words import word_list

chosen_word = random.choice(word_list)
word_length = len(chosen_word)

end_of_game = False
lives = 6

#TODO-3: - Import the logo from hangman_art.py and print it at the start of the game.
from hangman_art import logo
print(logo)

#Testing code
# print(f'Pssst, the solution is {chosen_word}.')

#Create blanks
display = []
for _ in range(word_length):
    display += "_"

while not end_of_game:
    guess = input("Guess a letter: ").lower()

    #TODO-4: - If the user has entered a letter they've already guessed, print the letter and let them know.
    if guess in display:
        print(f"You've already guessed {guess}")

    #Check guessed letter
    for position in range(word_length):
        letter = chosen_word[position]
        #print(f"Current position: {position}\n Current letter: {letter}\n Guessed letter: {guess}")
        if letter == guess:
            display[position] = letter

    #Check if user is wrong.
    if guess not in chosen_word:
        #TODO-5: - If the letter is not in the chosen_word, print out the letter and let them know it's not in the word.
        print(f"You guessed {guess}, that's not in the word. You lose a life.")
        
        lives -= 1
        if lives == 0:
            end_of_game = True
            print("You lose.")

    #Join all the elements in the list and turn it into a String.
    print(f"{' '.join(display)}")

    #Check if user has got all letters.
    if "_" not in display:
        end_of_game = True
        print("You win.")

    #TODO-2: - Import the stages from hangman_art.py and make this error go away.
    from hangman_art import stages
    print(stages[lives])
```
