---
title: "Bash Cheat sheet"
datePublished: Tue Jan 07 2025 14:12:04 GMT+0000 (Coordinated Universal Time)
cuid: cm5mjuqgv000909lddxtf9ub0
slug: bash-cheat-sheet
tags: linux, bash, shell, shell-script, shebang, bash-cheat-sheet

---

## Introduction to Shell

A **shell** is a command-line interface (CLI) that allows users to interact with the operating system by entering commands. It acts as an interpreter between the user and the system's kernel, translating commands into actions.

### Types of Shells

1. **Bourne Shell (sh)**: The original Unix shell.
    
2. **C Shell (csh)**: Syntax similar to the C programming language.
    
3. **Korn Shell (ksh)**: A superset of Bourne shell with added features.
    
4. **Z Shell (zsh)**: Feature-rich, supports plugins and themes.
    
5. **Bash Shell (bash)**: Bourne Again Shell, the most widely used shell.
    

---

## What is Bash?

Bash (Bourne Again Shell) is a Unix shell and command language. It is the default shell on most Linux distributions and macOS. Bash extends the capabilities of the Bourne shell (sh) with numerous enhancements.

### Major Features of Bash:

* **Command History**: Allows re-executing previously entered commands.
    
* **Tab Completion**: Auto-completes commands and file names.
    
* **Scripting**: Write scripts to automate tasks using loops, conditionals, and functions.
    
* **Command Substitution**: Execute a command and use its output as part of another command.
    
* **Job Control**: Suspend, resume, or terminate processes.
    

---

## Shebang (#!)

The **shebang** is the first line in a script that specifies the interpreter to execute the script. It starts with `#!` followed by the path to the interpreter.

Example:

```bash
#!/bin/bash
```

This tells the system to use the Bash shell to execute the script. Without a shebang, the script may not run as expected or rely on the user's default shell.

---

## How to Use Bash

### 1\. Opening Bash

* On Linux/macOS: Open a terminal application (e.g., GNOME Terminal, iTerm2).
    
* On Windows: Use Windows Subsystem for Linux (WSL) or Git Bash.
    

### 2\. Basic Commands

```bash
# Display the current working directory
pwd

# List files and directories
ls

# Change directory
cd <directory_path>

# Create a new file
touch <file_name>

# Create a new directory
mkdir <directory_name>

# Display file content
cat <file_name>

# Copy a file
cp <source_file> <destination>

# Move/Rename a file
mv <source_file> <destination>

# Delete a file or directory
rm <file_name>
rm -r <directory_name>  # Recursive delete for directories
```

### 3\. Variables

```bash
# Define a variable
my_var="Hello, Bash!"

# Access a variable
echo $my_var

# Read user input into a variable
read user_input
```

### 4\. Control Structures

#### If Statements

```bash
if [ condition ]; then
  # Commands to execute if condition is true
else
  # Commands to execute if condition is false
fi
```

Example:

```bash
if [ -f "file.txt" ]; then
  echo "File exists."
else
  echo "File does not exist."
fi
```

#### Loops

**For Loop:**

```bash
for i in 1 2 3; do
  echo "Number: $i"
done
```

**While Loop:**

```bash
while [ condition ]; do
  # Commands to execute while condition is true
done
```

### 5\. Functions

```bash
my_function() {
  echo "This is a function."
}

# Call the function
my_function
```

---

## Advanced Bash Commands

### Redirection

* Output to a file: `command > file`
    
* Append output to a file: `command >> file`
    
* Redirect errors: `command 2> error_file`
    
* Redirect output and errors: `command > file 2>&1`
    

### Piping

Send the output of one command as input to another:

```bash
ls -l | grep "pattern"
```

### Command Substitution

Use the output of a command:

```bash
current_date=$(date)
echo "Today is $current_date"
```

### Process Management

```bash
# View running processes
ps

# Kill a process
kill <PID>

# Background a process
command &

# Bring a background process to the foreground
fg
```

---

## Writing Bash Scripts

1. Create a script file with `.sh` extension:
    
    ```bash
    nano script.sh
    ```
    
2. Add the shebang line at the top to specify the interpreter:
    
    ```bash
    #!/bin/bash
    ```
    
3. Write your script commands. Example:
    
    ```bash
    #!/bin/bash
    echo "Hello, World!"
    ```
    
4. Make the script executable:
    
    ```bash
    chmod +x script.sh
    ```
    
5. Run the script:
    
    ```bash
    ./script.sh
    ```
    

---

## Useful Bash Shortcuts

* **Ctrl + A**: Move to the beginning of the line.
    
* **Ctrl + E**: Move to the end of the line.
    
* **Ctrl + U**: Clear the line before the cursor.
    
* **Ctrl + K**: Clear the line after the cursor.
    
* **Ctrl + R**: Search command history.
    

---

This cheat sheet is your quick reference to mastering Bash. Practice regularly and explore its full potential to automate and enhance your workflows.