## Love Calculator

You are going to write a program that tests the compatibility between two people.

To work out the love score between two people:

1. Take both people's names and check for the number of times the letters in the word TRUE occurs.
2. Then check for the number of times the letters in the word LOVE occurs.
3. Combine these numbers to make a 2-digit number.

For Love Scores less than 10 or greater than 90, the message should be:
"Your score is x, you go together like coke and mentos."

For Love Scores between 40 and 50, the message should be:
"Your score is y, you are alright together."

Otherwise, the message will just be their score. e.g.:
"Your score is z."


### Example 1

**Input:**
Kanye West
Kim Kardashian

**Output:**
The Love Calculator is calculating your score...
Your score is 42, you are alright together.

### Example 2

**Input:**
Brad Pitt
Jennifer Aniston

**Output:**
The Love Calculator is calculating your score...
Your score is 73.


#### Hint
You can check your values against mine using this table:

| Name 1           | Name 2              | Score |
|------------------|---------------------|-------|
| Brad Pitt        | Jennifer Aniston    | 73    |
| Prince William   | Kate Middleton      | 67    |
| Ashton Kutcher   | Mila Kunis          | 63    |
| Angela Yu        | Jack Bauer          | 53    |
| David Beckham    | Victoria Beckham    | 45    |
| Mario            | Princess Peach      | 43    |
| Kanye West       | Kim Kardashian      | 42    |

### Solution

```
print("The Love Calculator is calculating your score...")
name1 = input("What is your name? ")
name2 = input("What is their name? ")
true = "true"
love = "love"
combined_names = (name1 + name2).lower()  # Combine names and convert to lowercase
tense_count = 0
ones_count = 0

# Iterate through each character in combined_names
for char in combined_names:
    # Check if the character is in the string 'true'
    if char in true:
        tense_count += 10  # Increase tense_count by 10 for each match

    # Check if the character is in the string 'love'
    if char in love:
        ones_count += 1  # Increase ones_count by 1 for each match

# Calculate love score
love_score = tense_count + ones_count

# Output the result based on love_score
if love_score < 10 or love_score > 90:
    print(f"Your score is {love_score}, you go together like coke and mentos.")
elif 40 <= love_score <= 50:
    print(f"Your score is {love_score}, you are alright together.")
else:
    print(f"Your score is {love_score}.")
```
