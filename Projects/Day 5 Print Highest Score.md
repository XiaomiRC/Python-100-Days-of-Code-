# Instructions
You are going to write a program that calculates the highest score from a List of scores.

### Example:
```python
student_scores = [78, 65, 89, 86, 55, 91, 64, 89]
```
### Important
You are not allowed to use the max() or min() functions. The output words must match the example.

### Example Input
```
78 65 89 86 55 91 64 89
```
In this case, `student_scores` would be a list that looks like: `[78, 65, 89, 86, 55, 91, 64, 89]`

### Example Output
```kotlin
The highest score in the class is: 91
```

### Solution:
```python
# Input a list of student scores
student_scores = input("Enter student scores separated by space: ").split()

# Convert each score from string to integer
for n in range(0, len(student_scores)):
    student_scores[n] = int(student_scores[n])

# Initialize highest_score with 0
highest_score = 0

# Iterate through the scores to find the highest score
for score in student_scores:
    if score > highest_score:
        highest_score = score

# Output the highest score found
print(f"The highest score in the class is: {highest_score}")
```
