# Easy-Enroll Student Enrollment System

**Easy-Enroll** is a Java-based student enrollment system with a **client-server architecture**, GUI interfaces, and database connectivity. It allows students to browse and enroll in courses and provides administrators with tools to manage students and course offerings.

---

## 📋 Overview

The system demonstrates **core Java concepts**:

* GUI development with **Swing**
* **JDBC** database connectivity
* Socket-based **client-server communication**
* Object-oriented design and modular code architecture

Students and administrators access the system via separate GUIs, communicating with a central server that handles business logic and database operations.

---

## ✨ Key Features

* **Client-Server Architecture** – Centralized server manages database operations and business logic
* **Student Interface** – Browse courses and enroll with duplicate prevention
* **Admin Interface** – Add students/courses, view enrollments, manage data
* **Real-Time Communication** – Persistent TCP socket connections using ObjectInputStream/ObjectOutputStream
* **Data Validation** – Input validation both client-side and server-side
* **Layered Design** – GUI, client logic, server processing, and DAO layers separated for clarity

---

## 🛠️ Technologies Used

* **Java SE** – Core programming language
* **Java Swing** – GUI interfaces
* **Java Sockets** – Network communication
* **JDBC** – Database connectivity
* **Apache Derby** – Embedded relational database
* **Object Serialization** – Transmitting domain objects (Student, Course, Enrollment) over network

---

## ⚙️ System Architecture

### Client-Side

* **Client.java** – Handles socket connections and object streams, shared across GUI components
* **Login.java** – Authentication interface, role-based access
* **StudentGui.java** – Enroll in courses and view current enrollments
* **AdminGui.java** – Manage students, courses, and view enrollment information

### Server-Side

* **Server.java** – Processes client commands and coordinates DAO operations
* Command-based protocol (`login`, `enroll`, `getCourses`, etc.)
* Persistent connections allow multiple operations per session

### Data Access Layer (DAO)

* **LoginDAO.java** – Authentication
* **StudentDAO.java** / **CourseDAO.java** – Add and manage students/courses, prevent duplicates
* **EnrollDAO.java** – Handles course enrollments, batch processing for efficiency
* **DBConnection.java** – Centralized database connection management

### Domain Model

* **Student.java, Course.java, Enrollment.java** – Serializable POJOs representing core entities
* Encapsulates relationships and supports transmission over sockets

---

## 🎯 Key Learning Outcomes

* Implementation of a **client-server system** with sockets
* Building **interactive GUIs** with Swing
* Database operations using **JDBC** with proper resource management
* Serialization and network object transmission
* Modular and layered architecture for maintainable code

---

## 🚀 Future Enhancements

* **Multithreading** – Allow multiple simultaneous client connections
* **Logging Framework** – Replace print statements with structured logging
* **Configurable Parameters** – Database and server settings via external files
* **Enhanced Error Handling** – Specific error messages and exception management

---

*Built with **Java**, **Swing**, **JDBC**, and **Apache Derby***
