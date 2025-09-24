# Student Management System

A console-based student management system written in C for managing student records with CGPA calculation functionality.

## Features

- **Student Record Management**: Add, modify, display, and delete student records
- **Individual Student View**: Search and view specific student information
- **CGPA Calculation**: Automatically calculates CGPA from 12 semester SGPAs
- **Password Protection**: Login system with changeable password
- **File-based Storage**: Persistent data storage using binary files
- **User-friendly Interface**: Menu-driven system with clear options

## System Requirements

- Windows operating system (uses Windows-specific libraries)
- C compiler (GCC or similar)
- Console environment

## File Structure

- `db.txt` - Main database file storing student records
- `Password.txt` - File storing encrypted password (located at F:/)
- `temp.txt` - Temporary file used during delete operations

## How to Compile and Run

1. **Compile the program:**
   ```bash
   gcc student_management.c -o student_management
   ```

2. **Run the program:**
   ```bash
   ./student_management
   ```

3. **First Login:**
   - Press ENTER for first-time login
   - Set up your password when prompted

## Menu Options

### Main Menu
1. **Add Student** - Add new student records with SGPA data
2. **Modify Student** - Edit existing student information
3. **Show All Students** - Display all student records
4. **Individual View** - Search and view specific student by roll number
5. **Remove Student** - Delete student record by roll number
6. **Change Password** - Update login password
7. **Logout** - Exit the program

## Student Record Structure

Each student record contains:
- **Name**: Full name of the student
- **Department**: Department/Faculty name
- **Roll Number**: Unique identifier
- **SGPA Array**: Grades for 12 semesters
- **CGPA**: Calculated cumulative grade point average

## Usage Instructions

### Adding a Student
1. Select option 1 from main menu
2. Enter student's full name
3. Enter department name
4. Enter roll number
5. Input SGPA for all 12 semesters
6. CGPA will be calculated automatically

### Modifying Records
1. Select option 2 from main menu
2. Enter the roll number of student to modify
3. Update the information as prompted
4. Changes are saved automatically

### Viewing Records
- **All Students**: Option 3 displays all records
- **Individual**: Option 4 allows searching by roll number

### Deleting Records
1. Select option 5 from main menu
2. Enter roll number of student to delete
3. Confirm deletion when prompted

## Important Notes

- The program uses binary file storage for efficient data handling
- Password file is stored at `F:/Password.txt` by default
- CGPA is calculated as average of 12 semester SGPAs
- All input validation should be handled carefully
- Make sure to backup your `db.txt` file regularly

## Error Handling

The system handles common errors including:
- File creation/opening failures
- Invalid menu selections
- Record not found scenarios
- Password validation errors

## Security Features

- Password-protected access
- Password change functionality
- Secure file handling for student data

## Technical Details

- Written in C programming language
- Uses Windows console API for enhanced display
- Binary file operations for data persistence
- Structure-based data organization
- Menu-driven user interface
