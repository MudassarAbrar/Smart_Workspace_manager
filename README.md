
# 🌟 Smart Workspace Manager (SWM)

A modular **C++ console application** designed to manage **employees**, **departments**, and **meetings** within an organization.  
The system demonstrates **dynamic memory allocation**, **structured architecture**, **file persistence**, and **multi-module program design**.

---

## 📌 Table of Contents
1. [Overview](#overview)  
2. [Key Features](#key-features)  
3. [Project Structure](#project-structure)  
4. [Data Flow & Architecture](#data-flow--architecture)  
5. [Build Instructions](#build-instructions)  
6. [Running the Program](#running-the-program)  
7. [Data File Formats](#data-file-formats)  
8. [Module Responsibilities](#module-responsibilities)  
9. [Team Members & Work Division](#team-members--work-division)

---

## 📘 Overview

**Smart Workspace Manager** is a C++ application built to simulate a real-world office management system.

It efficiently handles:
- Employee records  
- Department data  
- Meeting scheduling  

The system uses **dynamic memory**, **modular code**, and **simple text file storage** to persist data across program runs.

---

## 🚀 Key Features

### 👨‍💼 Employee Management
- Add & remove employees  
- Update attendance and performance  
- Determine bonus eligibility  
- View complete employee details  
- Automatically link employee to department  

### 🏢 Department Management
- Create & delete departments  
- Store and track employee IDs  
- Display department details  
- Identify top performer  
- Compute average performance  
- Check department capacity  

### 📅 Meeting Management
- Create meetings with topic, date, and time  
- Check & prevent scheduling clashes  
- Add participants using employee IDs  
- Display meeting & participant details  

---

## 💾 Data Persistence

All data is automatically saved to:

```

employee.txt
departments.txt
meetings.txt

```

Data is reloaded every time the program starts.

---

## 📁 Project Structure

```

.
├── main.cpp                // Menu system and program flow
├── project.h               // Structs, constants, global declarations
├── global.cpp              // Memory allocation + global variables
├── employee.cpp            // Employee logic
├── department.cpp          // Department logic
├── meeting.cpp             // Meeting management logic
│
├── employee.txt            // Employee data
├── departments.txt         // Department data
├── meetings.txt            // Meeting data
│
└── README.md               // Project documentation

````

---

## 🧠 Data Flow & Architecture

### 1. **Global Resources (global.cpp)**
Handles dynamic memory and global state.

- Allocates arrays for:
  - Employees  
  - Departments  
  - Meetings  

- Stores counters:
  - `employee_count`
  - `department_count`
  - `meeting_count`

- Core functions:
  - `initializeMemory()`
  - `freeMemory()`

---

### 2. **Core Modules**

| File | Responsibility |
|------|---------------|
| **employee.cpp** | Employee CRUD, performance, bonus, department linking, file I/O |
| **department.cpp** | Department creation, capacity management, metrics, file I/O |
| **meeting.cpp** | Meetings, clash detection, participants, file persistence |
| **main.cpp** | Menu-driven interface and navigation |

---

### 3. **Struct & Header Definitions (project.h)**

Contains all shared structures:
- `Employee`  
- `Department`  
- `Meeting`

Also includes:
- Global pointers  
- Function prototypes  
- Shared constants  

---

## 🛠 Build Instructions

### **Linux / macOS**
```bash
g++ main.cpp global.cpp employee.cpp department.cpp meeting.cpp -o workspace_manager
````

### **Windows (MinGW / TDM-GCC)**

```bash
g++ main.cpp global.cpp employee.cpp department.cpp meeting.cpp -o manager.exe
```

---

## ▶ Running the Program

### Linux / macOS

```bash
./workspace_manager
```

### Windows

```bash
manager.exe
```

---

## 📂 Data File Formats

### **employee.txt**

```
emp_id emp_name dept_name salary attendance performance bonus_eligible
```

### **departments.txt**

```
dept_name employee_count emp_id_1 emp_id_2 ...
```

### **meetings.txt**

```
meet_id topic date time participant_count emp_id_1 emp_id_2 ...
```

---

## 🧩 Module Responsibilities

### ➤ employee.cpp

* Create/delete employees
* Manage attendance & performance
* Bonus calculation
* Link employee to department
* Load/save employee data

---

### ➤ department.cpp

* Create/delete departments
* Maintain employee lists
* Resize department capacity dynamically
* Identify top performer
* Calculate average performance
* Load/save department data

---

### ➤ meeting.cpp

* Create meetings
* Validate schedules
* Prevent time/date clashes
* Add participants
* Load & save meeting data

---

### ➤ main.cpp

* Menu-driven user interface
* Handles input routing
* Controls program execution

---

## 👥 Team Members & Work Division

### **Mudassir Abrar Baig**

**Roll No:** BCF23M035

---

### **Abdul Rahman Bin Abid**

**Roll No:** BCSF24M021

---

### **Zainab Irfan**

**Roll No:** BCSF24M013


---

## 🤝 Work Strategy

* Each member owned one major module
* All modules connected using shared header and global memory
* Team collaborated on:

  * Error handling
  * Naming conventions
  * File format design
* Final debugging and documentation done together

---

## ⭐ Final Notes

This project demonstrates:

* Modular C++ development
* Dynamic memory management
* Data persistence
* Realistic workplace simulation

Feel free to fork, improve, and extend the system!

```
```
