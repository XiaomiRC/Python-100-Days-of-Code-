# Question: Categorizing the Dirty Dozen
You have a list called dirty_dozen that contains various fruits and vegetables. Using Python, how would you modify this list to categorize its items into separate lists for fruits and vegetables? Provide the code snippet that accomplishes this task and explain your approach.
This question invites the respondent to demonstrate their understanding of list manipulation in Python, specifically focusing on categorizing items based on predefined criteria (fruits vs vegetables). It encourages them to provide a code snippet and explain their thought process, which tests both their coding skills and their ability to articulate their approach.

### Solution:

```python
# Original dirty dozen list
dirty_dozen = ["Strawberries", "Spinach", "Kale", "Nectarines", "Apples", "Grapes", "Peaches", "Cherries", "Pears", "Tomatoes", "Celery", "Potatoes"]
print("Original dirty dozen:")
print(dirty_dozen)

# Separate lists for fruits and vegetables
fruits = ["Strawberries", "Nectarines", "Apples", "Grapes", "Peaches", "Cherries", "Pears"]
vegetables = ["Spinach", "Kale", "Tomatoes", "Celery", "Potatoes"]

# Create a new structure with fruits and vegetables categorized
dirty_dozen_categorized = {
    "fruits": fruits,
    "vegetables": vegetables
}

print("\nDirty dozen categorized:")
print(dirty_dozen_categorized)
```

# Explanation

### Original List:
- `dirty_dozen` contains all the items listed together.

### Separation into Categories:
- Fruits and vegetables are separated based on their type.

### Categorization Structure:
- Instead of overwriting `dirty_dozen`, which might lead to confusion, a dictionary `dirty_dozen_categorized` is created to hold fruits and vegetables as separate lists under their respective keys.

### Output:
- The original `dirty_dozen` list is printed first to show its contents.
- Then, `dirty_dozen_categorized` is printed to show how the items are categorized into fruits and vegetables.

This approach ensures clarity and organization in managing and displaying the different categories of items in the `dirty_dozen` list.

