# Task Manager Application - Developer Guide

## 🔧 Overview

The **Task Manager Application** is a Java-based project that uses **Swing** for the GUI, implements file-based persistence with `.csv`, and provides task management features such as adding, editing, deleting, and categorizing tasks. It is designed for simplicity and efficiency.

---

## 📂 Project Structure

The project is organized as follows:

```
src/
├── Task.java          // Represents a single task
├── TaskCategory.java  // Enum for task categories (WORK, PERSONAL, OTHER)
├── TaskManager.java   // Handles the task list and task operations
├── FileManager.java   // Manages saving/loading tasks to/from a CSV file
├── TaskManagerUI.java // Swing-based GUI for the application
└── TaskManagerApp.java// Main entry point of the application
```

---

## ✨ Key Features

### 1. **Task Management**
   - Each task is represented by the `Task` class with attributes:
     - `String title`
     - `boolean isComplete`
     - `TaskCategory category`
   - Task status toggling and edits update the in-memory task list and UI.

### 2. **Persistence**
   - Tasks are saved to and loaded from a `.csv` file (`tasks.csv`).
   - Each line in the file represents a task with the format: `title,isComplete,category`.
   - File operations are handled by the `FileManager` class using `BufferedReader` and `BufferedWriter`.

### 3. **GUI**
   - Built using Java Swing.
   - Features include:
     - `JList` for displaying tasks.
     - Buttons for Add, Edit, Delete, and Toggle Complete.
     - Keyboard support for navigation (`Arrow Keys`) and toggling task status (`Spacebar`).
   - Styled using a Catppuccin-inspired theme with custom colors.

---

## 🔧 How to Build and Run

### 1. **Prerequisites**
   - Java Development Kit (JDK) version 8 or higher.
   - A Java IDE (e.g., IntelliJ IDEA, Eclipse) or a terminal with `javac`.

### 2. **Building the Project**
   - Clone the repository:
     ```bash
     git clone https://github.com/your-repo-link
     cd task-manager
     ```
   - Compile the source files:
     ```bash
     javac src/*.java -d out
     ```
   - Create an executable JAR:
     ```bash
     jar cfe TaskManagerApp.jar TaskManagerApp -C out .
     ```

### 3. **Running the Program**
   - Run the program with:
     ```bash
     java -jar TaskManagerApp.jar
     ```

---

## 🖒 Testing

### 1. **Manual Testing**
   - Verify basic operations:
     - Add, edit, delete tasks.
     - Toggle task status.
     - Navigation with arrow keys and spacebar.
   - Check `.csv` file contents after closing the application.

### 2. **Unit Testing**
   - Add JUnit tests for:
     - Task creation and status toggling.
     - File read/write operations in `FileManager`.
     - TaskManager methods like `addTask` and `deleteTask`.

---

## 🎨 Catppuccin Theme Implementation

### Theme Colors:
   - **Background**: `#1E272E`
   - **Foreground**: `#DFE4EA`
   - **Highlight**: `#FF9F43`
   - **Button**: `#636E72`

### Applying the Theme:
   - Background and foreground colors are set for `JList`, buttons, and panels.
   - Fonts are customized for a modern, aesthetic look.

---

## 🔗 Contributions

Contributions are welcome! Follow these steps:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature description"
   ```
4. Push the branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

---

## 🐜 License

This project is licensed under the [MIT License](LICENSE).

For more details or issues, contact [konstantin@wbauer.com](mailto:konstantin@wbauer.com).

