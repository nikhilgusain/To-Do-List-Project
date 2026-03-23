# 📝 Java Swing To-Do List Application

A robust, desktop-based To-Do List manager built with Java Swing and JDBC. This application allows users to create tasks, track due dates, mark tasks as complete, and manage their daily workflows through a clean graphical interface, with all data persistently stored in a MySQL database.

## ✨ Features

* **Add Tasks:** Create new tasks with specific due dates.
* **View All Tasks:** View a comprehensive tabular list of all tasks, including their IDs, addition times, completion dates, and current statuses.
* **Mark as Complete:** Update a task's status to "Completed" using its unique Task ID.
* **Delete Tasks:** Remove specific tasks from the database using their Task ID.
* **Clear Completed:** A one-click utility to sweep and delete all successfully completed tasks from the database.

## 🗂️ Project Structure

* `Main.java`: The entry point that initializes the application.
* `ToDoListGUI.java`: Contains the Java Swing frontend components, event listeners, and dialog windows.
* `ToDoListDAO.java`: The Data Access Object handling database interactions, SQL queries, and result parsing.
* `DB_Connection.java`: Manages the JDBC connection to the local MySQL instance.

## 🛠️ Prerequisites

To run this application, you will need:
1.  **Java Development Kit (JDK):** Version 8 or higher.
2.  **MySQL Server:** Running locally on port `3306`.
3.  **MySQL JDBC Driver:** `mysql-connector-j.jar` added to your project's classpath.

## 🚀 Setup & Installation

1.  **Database Configuration:**
    * Open your MySQL environment.
    * Create a database named `todo_db`.
    * Create a table named `tasks` with the necessary columns (`taskID` as Primary Key/Auto-Increment, `task`, `dueDate`, `addedDate`, `addedTime`, `completionDate`, `status`).
2.  **Update Credentials:**
    * Open `DB_Connection.java`.
    * Ensure the `user` and `pass` variables match your local MySQL credentials.
3.  **Compile and Run:**
    * Compile the Java files ensuring the JDBC driver is in the classpath.
    * Run the `Main` class to launch the GUI.

## 🖥️ Usage

* Click **Add task** and enter your task description along with the date in `YY-MM-DD` format.
* Click **Show All Tasks** to find the ID of a specific task.
* Use the **Complete Task** or **Delete Task** buttons by providing the corresponding Task ID.
