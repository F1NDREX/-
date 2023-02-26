from tkinter import *
import random

window = Tk()
window.geometry("500x500")


def triangle():
    canvas.create_line(100, 370, 310, 370)
    canvas.create_line(100, 370, 230, 250)
    canvas.create_line(230, 250, 310, 370)


def rectangle():
    canvas.create_rectangle(80, 180, 310, 370)


def oval():
    canvas.create_oval(80, 180, 310, 370)


def change():
    canvas.delete('all')
    functions = (triangle, rectangle, oval)
    choice = random.choice(functions)
    choice()


button = Button(window, text="Random", command=change)
button.pack()

canvas = Canvas(window, height=500, width=500)
canvas.pack()

window.mainloop()
