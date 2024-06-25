# Dice-Rolling-game
Dice rolling game in python using turtle library
import turtle
import random

# Set up the turtle screen
wn = turtle.Screen()
wn.setup(500, 500)
wn.title("Rolling Dice Game")

# Create the dice object
dice = turtle.Turtle()
dice.hideturtle()
dice.penup()

# Draw the outline of the dice
def draw_dice():
    dice.clear()
    dice.goto(45, -45)
    dice.pendown()
   
    for i in range(4):
        dice.backward(100)
        dice.right(90)
    dice.penup()
    dice.goto(110, 110)
    dice.pendown()
    for i in range(4):
        dice.forward(2)
        dice.left(90)
    dice.penup()

    
# Roll the dice and display the result
def roll_dice():
    draw_dice()
    number = random.randint(1, 6)
    wn.bgcolor("pink")
    if number == 1:
        dice.goto(0, 0)
        dice.dot(10)
    elif number == 2:
        dice.goto(-20, 20)
        dice.dot(10)
        dice.goto(20, -20)
        dice.dot(10)
    elif number == 3:
        dice.goto(-20, 20)
        dice.dot(10)
        dice.goto(0, 0)
        dice.dot(10)
        dice.goto(20, -20)
        dice.dot(10)
    elif number == 4:
        dice.goto(-20, 20)
        dice.dot(10)
        dice.goto(20, 20)
        dice.dot(10)
        dice.goto(-20, -20)
        dice.dot(10)
        dice.goto(20, -20)
        dice.dot(10)
    elif number == 5:
        dice.goto(-20, 20)
        dice.dot(10)
        dice.goto(20, 20)
        dice.dot(10)
        dice.goto(0, 0)
        dice.dot(10)
        dice.goto(-20, -20)
        dice.dot(10)
        dice.goto(20, -20)
        dice.dot(10)
    elif number == 6:
        dice.goto(-20, 20)
        dice.dot(10)
        dice.goto(20, 20)
        dice.dot(10)
        dice.goto(-20, 0)
        dice.dot(10)
        dice.goto(20, 0)
        dice.dot(10)
        dice.goto(-20, -20)
        dice.dot(10)
        dice.goto(20, -20)
        dice.dot(10)

# Bind the roll_dice() function to the space key
wn.onkeypress(roll_dice, "space")
wn.listen()

# Start the main event loop
turtle.mainloop()
