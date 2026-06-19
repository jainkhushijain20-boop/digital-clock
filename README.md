# digital-clock
A simple Digital Clock application built using Python and Tkinter. This project displays the current time and date in real-time with an easy-to-use graphical user interface (GUI). The clock updates automatically every second and provides an accurate digital time display.
import tkinter as tk
from time import strftime

root = tk.Tk()
root.title("Digital Clock")

def time():
    string = strftime("%H:%M:%S %p\n%D")
    label.config(text=string)
    label.after(1000, time)

label = tk.Label(
    root,
    font=('calibri', 50, 'bold'),
    background='yellow',
    foreground='black'
)

label.pack(anchor='center')

time()

root.mainloop()
