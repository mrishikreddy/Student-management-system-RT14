# Student Information Portal

Welcome to the **Student Information Portal**, a C-based console application designed to manage student records efficiently. This project provides a user-friendly interface to add, search, update, delete, and display student information, as well as calculate the average GPA of all students. It's an ideal tool for academic institutions or anyone looking to organize student data in a simple yet effective way.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Acknowledgements](#acknowledgements)

## Features
- **Add Student Records**: Input details for one or multiple students, including ID, name, program, age, and GPA.
- **Search Students**: Find a student by their ID and view their details.
- **Update Records**: Modify existing student information.
- **Delete Records**: Remove individual student records or clear the entire database.
- **Display All Records**: View a list of all students with their details.
- **Calculate Average GPA**: Compute the average GPA across all students.
- Simple console-based interface with clear prompts and navigation.
- Dynamic memory management using a linked list for efficient storage.

## Installation
To set up the **Student Information Portal**, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/student-information-portal.git
   cd student-information-portal
   ```

2. **Compile the Code**:
   Ensure you have a C compiler installed (e.g., GCC). Compile the source code using:
   ```bash
   gcc -o student_portal main.c
   ```

3. **Run the Program**:
   On Windows:
   ```bash
   student_portal.exe
   ```
   On Linux/Mac:
   ```bash
   ./student_portal
   ```

   **Note**: The program uses `system("cls")` for screen clearing, which is Windows-specific. For Linux/Mac, replace it with `system("clear")` or remove it for portability. The code is otherwise cross-platform compatible as it uses standard C libraries (`stdio.h`, `stdlib.h`, `string.h`).

## Usage
Upon running the program, you'll be greeted with the main menu:
```
                WELCOME TO STUDENT INFORMATION PORTAL
                -------------------------------------

                enter:
                1 to add student information
                2 to search a student information
                3 to update a student information
                4 to know the average GPA of all students
                5 to display the entire record
                6 to delete a student information
                7 to clear entire record
                8 to exit

                your choice:
```
- Enter a number (1–8) to select an option.
- Follow the on-screen prompts to input or retrieve data.
- The program runs in a loop, allowing you to perform multiple operations until you choose to exit (option 8).

## How It Works
The program uses a singly linked list to store student records, where each node contains:
- Student ID (integer)
- Full Name (string)
- Program (string)
- Age (integer)
- GPA (float)

### Key Functions
- **Add (`add()`)**: Prompts for the number of students to add, then collects details for each (ID, name, program, age, GPA). New records are appended to the linked list.
- **Search (`search()`)**: Finds a student by ID and displays their details, or notifies if the ID is not found.
- **Update (`update()`)**: Locates a student by ID and allows editing of all their details.
- **Delete (`delp()` and `delt()`)**:
  - `delp()`: Removes a single student by ID.
  - `delt()`: Clears the entire linked list (formats the record).
- **Display (`display()`)**: Lists all students with their details in a formatted manner.
- **Average GPA (`average()`)**: Calculates the average GPA of all students by summing their GPAs and dividing by the number of students.

### Data Structure
The program uses a linked list (`struct node`) for dynamic storage. Each node holds student data and a pointer to the next node. The `start` pointer tracks the list's head. Memory is allocated dynamically using `malloc` and freed appropriately during deletion.

### Error Handling
- Checks for empty lists before performing operations.
- Validates input for adding students (ensures size ≥ 1).
- Notifies users if a student ID is not found during search, update, or deletion.
- Handles invalid menu choices with an error message.

## Acknowledgements
- Built with ❤️ for academic management.
- Thanks to the C programming community for inspiration and resources.
- Special appreciation to contributors and users who help improve this project.

---

Explore the **Student Information Portal** and make it your own! If you have questions, suggestions, or issues, feel free to open an issue on GitHub. Happy managing!
