# Student Record Management System

A Flask-based web application demonstrating efficient student record management using multiple data structures.

## Data Structures Used

| Data Structure | Purpose | Justification |
|---------------|---------|---------------|
| **Hash Table** | Store and search student records | Provides O(1) average time complexity for search operations by student ID, making lookups extremely fast |
| **Linked List** | Sequential storage of students | Allows dynamic memory allocation and efficient insertion without pre-allocating array size |
| **Stack** | Undo delete operations | LIFO structure perfect for implementing undo functionality - last deleted student can be restored first |
| **Queue** | Process registration requests | FIFO structure ensures fair processing - students are handled in the order they registered |

## Features

1. **Add Student Record** - Add new students with ID, name, program, and year
2. **Search Student** - Fast O(1) search using student ID via hash table
3. **Update Student Information** - Modify existing student details
4. **Delete Student Record** - Remove students with undo capability
5. **Display All Students** - View complete list via linked list traversal
6. **Undo Delete** - Restore last deleted student using stack
7. **Registration Queue** - Manage student registration requests in FIFO order

## Installation

1. Install Flask:
```bash
pip install flask
```

2. Run the application:
```bash
python app.py
```

3. Open browser and navigate to:
```
http://127.0.0.1:5000
```

## Project Structure

```
├── app.py                 # Flask application and routes
├── data_structures.py     # Data structure implementations
├── templates/
│   ├── base.html         # Base template
│   ├── index.html        # Home page
│   ├── add_student.html  # Add student form
│   ├── search_student.html # Search functionality
│   ├── update_student.html # Update form
│   └── queue.html        # Registration queue
└── README.md
```

## Technical Implementation

- **Hash Table**: Python dictionary for O(1) student lookup
- **Linked List**: Custom Node class with next pointers for sequential storage
- **Stack**: Array-based implementation for undo operations
- **Queue**: Array-based FIFO implementation for registration processing

## Usage Examples

1. Add students through the "Add Student" page
2. Search for specific students by ID
3. Update student information as needed
4. Delete students (can be undone using "Undo Delete")
5. Add student IDs to registration queue and process them in order
