# HOSTEL-COMPLAINT-MANAGEMENT-SYSTEM
[hostel_complaint_management_system_readme.md](https://github.com/user-attachments/files/34323671/hostel_complaint_management_system_readme.md)
# Hostel Complaint Management System

A robust, console-based application written in **C** designed to efficiently manage student hostel complaints, track their resolution status, and generate analytical reports using dynamic memory allocation and binary file persistence.

---

## Features

* **Student & Complaint Registration:** Register new complaints with student details (UID, Name, Room Number, Contact) and categorized issues (Electricity, Water Supply, Room Cleaning, Furniture, Wi-Fi, Other).
* **Automatic ID Generation:** Automatically assigns unique, incremental Complaint IDs starting from `1001`.
* **Dynamic Memory Management:** Employs dynamic arrays (`realloc`) to efficiently handle memory allocation, scaling capacity as records grow.
* **Persistent Storage:** Automatically saves and loads complaint records using binary files (`complaints.dat`) to ensure data retention across system restarts.
* **Status Tracking & Updates:** Update complaint statuses dynamically through stages: `Pending`, `In Progress`, and `Resolved`.
* **Search & Delete:** Instantly lookup complaints by their unique ID or remove resolved/invalid entries.
* **Analytical Reports:** Generates statistical summaries, including total complaints, status breakdowns, and overall resolution percentages.

---

## Project Structure

```text
├── complaints.dat          # Binary data file (auto-generated upon runtime)
├── main.c                  # Main C source code file
└── README.md               # Project documentation
```

---

## Getting Started

### Prerequisites
You need a standard **C Compiler** (such as GCC, Clang, or MSVC) installed on your system.

### Compilation
Open your terminal or command prompt, navigate to the directory containing the source code, and run:

```bash
gcc main.c -o hostel_system
```

### Execution
Run the compiled executable:

* **On Linux / macOS:**
  ```bash
  ./hostel_system
  ```

* **On Windows:**
  ```cmd
  hostel_system.exe
  ```

---

## Main Menu Options

1. **Register New Complaint:** Input student details and select a complaint category.
2. **View All Complaints:** Display a formatted list of all registered complaints and their details.
3. **Search Complaint:** Search for a specific record using its unique Complaint ID.
4. **Update Complaint Status:** Modify the status of a complaint (`Pending` $\rightarrow$ `In Progress` $\rightarrow$ `Resolved`).
5. **Delete Complaint:** Remove a complaint record permanently from the system.
6. **Generate Complaint Report:** View a statistical summary of complaint statuses and resolution rates.
7. **Exit:** Save all changes, free allocated memory, and exit the application.
<img width="1600" height="1000" alt="WhatsApp Image 2026-11-04 at 1 08 56 PM" src="https://github.com/user-attachments/assets/2c2c7d70-633c-4e7e-9bab-c10b8e71078a" />

<img width="1600" height="1000" alt="WhatsApp Image 2026-11-04 at 1 08 56 PM (1)" src="https://github.com/user-attachments/assets/f404bdf5-1597-49bd-8543-6e9b4a999c93" />
<img width="1600" height="1000" alt="WhatsApp Image 2026-11-04 at 1 08 56 PM (2)" src="https://github.com/user-attachments/assets/0327fdf6-31c7-4cd3-8dea-682d628261a7" />

<img width="1600" height="1000" alt="WhatsApp Image 2026-11-04 at 1 08 56 PM (3)" src="https://github.com/user-attachments/assets/c9b8c633-a2b2-4c50-9fec-9b3b08808a4e" />



---

## Key Technical Highlights

* **Data Structures:** Utilizes nested C structures (`Student` nested inside `Complaint`) for modular data organization.
* **Buffer Safety:** Includes a custom `clearInputBuffer()` utility to prevent input buffer overflow issues when mixing `scanf` and `fgets`.
* **Safe Dynamic Reallocation:** Checks for `NULL` pointers during memory reallocation to prevent memory corruption and segmentation faults.
