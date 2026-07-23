# Student Management System

A simple console-based Student Management System built using Java. This program allows users to manage student records through a menu-driven interface.

## Features

- Add Student
- View Students
- Search Student by ID
- Edit Student Information
- Delete Student
- Clear All Students
- Exit Program

## Student Information

Each student record contains:
- Student ID
- Name
- Age
- Gender
- Course

## Validation

- Student ID format: `YYYY-NNNN-L` (Example: `2025-0115-K`)
- No duplicate Student IDs
- Name accepts letters and spaces only
- Age must be between **15 and 35**
- Gender: `M` or `F`
- Course selected by number

## How to Run

Compile the program:

```bash
javac Main.java
