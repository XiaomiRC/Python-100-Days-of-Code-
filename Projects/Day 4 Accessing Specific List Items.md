# Predicting Output of Python Code

### Given Code:
```python
fruits = ["Strawberries", "Nectarines", "Apples", "Grapes", "Peaches", "Cherries", "Pears"]
vegetables = ["Spinach", "Kale", "Tomatoes", "Celery", "Potatoes"]

dirty_dozen = [fruits, vegetables]
print(dirty_dozen[0])
print(dirty_dozen[1])
print(dirty_dozen[1][2])
print(dirty_dozen[1][3])
print(dirty_dozen[1][1])
```
### Question:
What do you think will be printed by the code snippet above?

### Explanation:
- **Lists Definition**:
  - `fruits` contains: ["Strawberries", "Nectarines", "Apples", "Grapes", "Peaches", "Cherries", "Pears"].
  - `vegetables` contains: ["Spinach", "Kale", "Tomatoes", "Celery", "Potatoes"].

- **Creating `dirty_dozen`**:
  - `dirty_dozen` is a list containing `fruits` and `vegetables` as its elements: `[fruits, vegetables]`.

- **Printing Elements**:
  - `print(dirty_dozen[0])` prints the first element of `dirty_dozen`, which is `fruits`.
  - `print(dirty_dozen[1])` prints the second element of `dirty_dozen`, which is `vegetables`.
  - `print(dirty_dozen[1][2])` prints the third item in `vegetables`, which is `"Tomatoes"`.
  - `print(dirty_dozen[1][3])` prints the fourth item in `vegetables`, which is `"Celery"`.
  - `print(dirty_dozen[1][1])` prints the second item in `vegetables`, which is `"Kale"`.


