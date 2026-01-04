# Digital Clock (Python)

A beginner-friendly Python digital clock built using Tkinter that displays the current system time in real time.

## Features
- Displays current system time
- Updates every second
- Built using Python Tkinter

## Code
```python
from tkinter import *
from time import strftime

root = Tk()
root.title("Digital Clock")

def time():
    string = strftime('%H:%M:%S %p')
    label.config(text=string)
    label.after(1000, time)

label = Label(
    root,
    font=('calibri', 40, 'bold'),
    background='black',
    foreground='white'
)

label.pack(anchor='center')

time()
root.mainloop()

