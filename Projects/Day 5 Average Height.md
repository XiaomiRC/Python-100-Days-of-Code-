# Instructions
You are going to write a program that calculates the average student height from a List of heights.

### Example:
```python
student_heights = [180, 124, 165, 173, 189, 169, 146]
```
The average height can be calculated by adding all the heights together and dividing by the total number of heights.
### Example Calculation:
```css
180 + 124 + 165 + 173 + 189 + 169 + 146 = 1146

There are a total of 7 heights in student_heights.

1146 ÷ 7 = 163.71428571428572

Average height rounded to the nearest whole number = 164
```
### Important
You should not use the sum() or len() functions in your answer. You should try to replicate their functionality using what you have learnt about for loops.

### Example Input 1
```
156 178 165 171 187
```
In this case, `student_heights` would be a list that looks like: `[156, 178, 165, 171, 187]`

### Example Output 1
```java
total height = 857
number of students = 5
average height = 171
```
### Example Input 2
```
151 145 179
```
### Example Output 2
```java
total height = 475
number of students = 3
average height = 158
```
### Solution:
```python
# Input a Python list of student heights
student_heights = input("Enter student heights separated by space: ").split()

# Convert each height from string to integer
for n in range(0, len(student_heights)):
    student_heights[n] = int(student_heights[n])

# Initialize variables for total height and number of students
total_height = 0
no_of_students = 0

# Calculate total height and number of students
for height in student_heights:
    total_height += height
    no_of_students += 1

# Calculate average height (rounded to the nearest integer)
average_height = round(total_height / no_of_students)

# Output results
print(f"Total height = {total_height}")
print(f"Number of students = {no_of_students}")
print(f"Average height = {average_height}")
```
