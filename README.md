import tkinter as tk

# Create the root window
root = tk.Tk()

# Define the questions
questions = [
    "What City were you born in?",
    "What is your favorite food?",
    "What was your 1st car?",
    "What is your Brother/Sister middle name?"
]

# Create a dictionary to store the answers
answers = {}

# Function to print the answers
def print_answers():
    for question, entry in answers.items():
        print(f"{question}: {entry.get()}")

# Create the form
for question in questions:
    # Create a label for the question
    label = tk.Label(root, text=question)
    label.pack()

    # Create an entry for the answer
    entry = tk.Entry(root)
    entry.pack()

    # Store the entry in the dictionary
    answers[question] = entry

# Create a button to submit the form
submit_button = tk.Button(root, text="Submit", command=print_answers)
submit_button.pack()

# Run the event loop
root.mainloop()
