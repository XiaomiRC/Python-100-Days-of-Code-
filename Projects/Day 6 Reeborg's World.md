### Hurdle 3
### Solution:
```
def turn_right():
    turn_left()
    turn_left()
    turn_left()

def jump():
    turn_left()  
    move()
    turn_right()
    move()
    turn_right()
    move()
    turn_left()

while not at_goal():    
    if wall_in_front():
        jump()
    else:
        move()

```
### Hurdle 4 
Link - [worlds%2Ftutorial_en%2Fhurdle4.json](https://reeborg.ca/reeborg.html?lang=en&mode=python&menu=worlds%2Fmenus%2Freeborg_intro_en.json&name=Hurdle%204&url=worlds%2Ftutorial_en%2Fhurdle4.json)
### Solution:
```
def turn_right():
    turn_left()
    turn_left()
    turn_left()

def jump():
    turn_left()
    while wall_on_right():
        move()
    turn_right()
    move()
    turn_right()
    while front_is_clear():
        move()
    turn_left()

while not at_goal():    
    if wall_in_front():
        jump()
    else:
        move()
```
### Maze
### Solution:
```
def turn_right():
    turn_left()
    turn_left()
    turn_left()

while front_is_clear():
    move()
turn_left()

while not at_goal():    
    if right_is_clear():
        turn_right()
        move()
    elif front_is_clear():
        move()
    else:
        turn_left()
```
