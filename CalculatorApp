import tkinter as tk

# Function to update the display when a button is clicked
def button_click(number):
    if number=='c':
        entry.delete(0,tk.END)
    else:
      current = entry.get()
      entry.delete(0, tk.END)
      entry.insert(0, current + str(number))
    
    

# Function to perform calculations
def calculate():
    current = entry.get()
    try:
        result = eval(current)
        entry.delete(0, tk.END)
        entry.insert(0, result)
    except Exception:
        entry.delete(0, tk.END)
        entry.insert(0, "Error")

# Create the main window
app = tk.Tk()
app.title("Simple Calculator")

# Entry widget to display the input and result
entry = tk.Entry(app, width=15,font=("Arial",15),justify="right")
entry.grid(row=0, column=0, columnspan=4,padx=20,pady=10)

# Define the buttons
buttons = [
    '7', '8', '9', '/',
    '4', '5', '6', '*',
    '1', '2', '3', '-',
    '0', '.', '+', '=',
    'c'
]

row_val = 1
col_val =0
# Create and place the buttons
for button in buttons:
    tk.Button(app, text=button, padx=20, pady=20, command=lambda b=button: button_click(b) if b != '=' else calculate()).grid(row=row_val, column=col_val)
    col_val += 1
    if col_val > 3:
        col_val = 0
        row_val += 1

# Start the GUI main loop
app.mainloop()
