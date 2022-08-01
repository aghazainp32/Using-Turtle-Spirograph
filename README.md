# Using-Turtle-Spirograph
Using Turtle library programming(GUI) based Spirograph
import turtle as t
from turtle import Screen
import random
timmy = t.Turtle()
t.colormode(255)

def random_color():
    r = random.randint(0, 255)
    g = random.randint(0, 255)
    b = random.randint(0, 255)
    color = (r, g ,b)
    return color

timmy.shape("turtle")
screen = Screen()
timmy.speed("fastest")

def draw_spirograph(size_of_gap):
    for _ in range(int(360/size_of_gap)):
        timmy.color(random_color())
        timmy.circle(100)
        current_heading = timmy.heading()
        timmy.setheading(current_heading + 10)

draw_spirograph(5)


screen.exitonclick()
