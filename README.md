from tkinter import *
from tkinter.tk import *

from time import strftime


root = Tk()
root.title('CSE A B Clock')

def time():
    string = strftime(‘%A %d %B , %I:%M:%S %p')
    lbl.config(text=string)
    lbl.after(1000, time)

lbl = Label(root, font=('aRIAL’, 40, 'bold'),
            background='purple',
            foreground='white')

lbl.pack(anchor='center')
time()

mainloop()
