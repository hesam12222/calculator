# calculator

from tkinter import *

root = Tk()

root.title("calculator")

root.geometry("450x600")

root.resizable(width=False, height=False)

root.configure(bg="black")

display = Label(root, font=("Arial", 45))
display.place(x=20, y=20, width=410, height=170)


def add_num(number):
    old_text = display.cget("text")
    display.config(text=old_text + str(number))


def clear():
    display.config(text="")


def cal():
    try:
        expression = display.cget("text")
        result = eval(expression)

        display.config(text=str(result))
    except:
        display.config(text="error")


b1 = Button(root, text="*", command=lambda:
add_num("*"), font=("Arial", 35), fg="orange", bg="gray77", bd=3, activebackground="gray")
b1.place(y=200, x=345, width=100, height=70)

b2 = Button(root, text="+", command=lambda:
add_num("+"), font=("Arial", 35), fg="orange", bg="gray77", bd=3, activebackground="gray")
b2.place(y=270, x=345, width=100, height=70)

b3 = Button(root, text="-", command=lambda:
add_num("-"), font=("Arial", 45), fg="orange", bg="gray77", bd=3, activebackground="gray")
b3.place(y=340, x=345, width=100, height=70)

b4 = Button(root, text="÷", command=lambda:
add_num("/"), font=("Arial", 35), fg="orange", bg="gray77", bd=3, activebackground="gray")
b4.place(y=410, x=345, width=100, height=70)

b5 = Button(root, text="=", command=cal, font=("Arial", 35), fg="orange", bg="aqua", bd=3, activebackground="gray")
b5.place(y=480, x=345, width=100, height=70)

# 7 8 9

b6 = Button(root, text="7", command=lambda:
add_num("7"), font=("Arial", 25), fg="black", bg="aqua", bd=3, activebackground="gray")
b6.place(y=200, x=20, width=100, height=70)

b7 = Button(root, text="8", command=lambda:
add_num("8"), font=("Arial", 25), fg="black", bg="aqua", bd=3, activebackground="gray")
b7.place(y=200, x=125, width=100, height=70)

b8 = Button(root, text="9", command=lambda:
add_num("9"), font=("Arial", 25), fg="black", bg="aqua", bd=3, activebackground="gray")
b8.place(y=200, x=230, width=100, height=70)

# 4 5 6

b9 = Button(root, text="4", command=lambda:
add_num("4"), font=("Arial", 25), fg="black", bg="aqua", bd=3, activebackground="gray")
b9.place(y=270, x=20, width=100, height=70)

b10 = Button(root, text="5", command=lambda:
add_num("5"), font=("Arial", 25), fg="black", bg="aqua", bd=3, activebackground="gray")
b10.place(y=270, x=125, width=100, height=70)

b11 = Button(root, text="6", command=lambda:
add_num("6"), font=("Arial", 25), fg="black", bg="aqua", bd=3, activebackground="gray")
b11.place(y=270, x=230, width=100, height=70)

# 1 2 3

b12 = Button(root, text="1", command=lambda:
add_num("1"), font=("Arial", 25), fg="black", bg="aqua", bd=3, activebackground="gray")
b12.place(y=340, x=20, width=100, height=70)

b13 = Button(root, text="2", command=lambda:
add_num("2"), font=("Arial", 25), fg="black", bg="aqua", bd=3, activebackground="gray")
b13.place(y=340, x=125, width=100, height=70)

b14 = Button(root, text="3", command=lambda:
add_num("3"), font=("Arial", 25), fg="black", bg="aqua", bd=3, activebackground="gray")
b14.place(y=340, x=230, width=100, height=70)

# 0 . C

b15 = Button(root, text="0", command=lambda:
add_num("0"), font=("Arial", 25), fg="black", bg="aqua", bd=3, activebackground="gray")
b15.place(y=410, x=125, width=100, height=70)

b16 = Button(root, text=".", command=lambda:
add_num("."), font=("Arial", 35), fg="black", bg="aqua", bd=3, activebackground="gray")
b16.place(y=410, x=230, width=100, height=70)

b17 = Button(root, text="c", command=clear, font=("Arial", 35), fg="black", bg="aqua", bd=3, activebackground="gray")
b17.place(y=410, x=20, width=100, height=70)

root.mainloop()

