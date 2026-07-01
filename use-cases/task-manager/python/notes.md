Task_Manager

The application does not use an interactive menu. Instead, it uses a command-based CLI interface powered by argument parsing (argparse). Each command triggers specific functionality in the application

Example 
python -m python.cli create "My first task"
Output 
Created task with ID: 0b401073-bd7b-4e3e-a7e1-410bd8123dd8

Interaction breakdown:


cli.py:

Parses user commands using argparse
Decides which action to execute


app.py:

Contains application logic
Calls functions to create/update/delete tasks

models.py :

Defines the structure of a task (e.g., ID, status, priority)
Ensures consistency of task data

storage.py :

Saves and loads tasks
Handles persistence (likely file-based)