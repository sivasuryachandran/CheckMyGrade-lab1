# CheckMyGrade-lab1
Lab Assignment - A Python console app for managing students, courses, professors, and grades — includes encryption, stats, and CSV persistence.


---

```
# 🧮 CheckMyGrade – Student Grade Management App

A lightweight **Python console application** for managing **students, professors, courses, and grades**, built for academic evaluation and experimentation.  
It uses **CSV persistence** (no database required) and demonstrates **CRUD**, **encryption**, **sorting/search performance**, and **statistics**.

---

## 🚀 Features

✅ **Student, Professor & Course Management**
- Add, update, delete, and view students, professors, and courses  
- Automatically calculates average and median marks per course  

✅ **File-Based Storage**
- Data stored in `students.csv`, `courses.csv`, `professors.csv`, and `login.csv`  
- Auto-creates valid CSV headers and handles corrupted/missing files gracefully  

✅ **Encryption**
- Passwords in `login.csv` are stored using a reversible XOR + Base64 cipher (for learning purposes only)

✅ **Performance Tracking**
- Measures and prints execution time for search and sort operations  

✅ **Unit Testing**
- Includes unittests for CRUD, encryption, persistence, and performance

✅ **Seeded Demo Data**
- Automatically seeds **3 courses**, **3 professors**, and **5 students** using the names of **Indian cricketers (men & women)**

---

## 🧑‍💻 Sample Data

| Role | Name | Course | Example Email |
|------|------|---------|----------------|
| Professor | Jhulan Goswami | Data Science (`DATA200`) | `jhulan@mycsu.edu` |
| Professor | Kapil Dev | Intro CS (`CS101`) | `kapil@mycsu.edu` |
| Professor | Anil Kumble | Statistics I (`STAT150`) | `kumble@mycsu.edu` |
| Student | Smriti Mandhana | Data Science | `smriti.mandhana@mycsu.edu` |
| Student | Harmanpreet Kaur | Intro CS | `harmanpreet.kaur@mycsu.edu` |
| Student | Mithali Raj | Statistics I | `mithali.raj@mycsu.edu` |
| Student | Virat Kohli | Data Science | `virat.kohli@mycsu.edu` |
| Student | Rohit Sharma | Intro CS | `rohit.sharma@mycsu.edu` |

---

## 🧩 Folder Structure

```

CheckMyGrade-App/
│
├── checkmygrade.py          # Main Python script (no GUI)
├── students.csv             # Student records
├── courses.csv              # Course details
├── professors.csv           # Professor info
├── login.csv                # Encrypted login data
├── README.md                # You’re reading this file
└── .gitignore               # Git ignore rules

````

---

## ⚙️ Setup & Run

### 🐍 Prerequisites
- Python 3.9+
- Works in local environments and Google Colab

### ▶️ Run Demo
```bash
python checkmygrade.py
````

This will:

* Reset CSV files
* Add 3 courses, 3 professors, and 5 students
* Display a formatted summary with average/median marks and search/sort timings

---

## 📊 Sample Output

```
CSV folder: /content
Files:
 - /content/students.csv
 - /content/courses.csv
 - /content/professors.csv
 - /content/login.csv

=== Courses ===
DATA200: Data Science (3 cr)
CS101: Intro CS (4 cr)
STAT150: Statistics I (3 cr)

=== Professors (by course) ===
Jhulan Goswami [Senior Professor] -> DATA200
Kapil Dev [Professor] -> CS101
Anil Kumble [Associate Prof.] -> STAT150

=== Students ===
Smriti Mandhana <smriti.mandhana@mycsu.edu> | DATA200 | A (95)
Virat Kohli <virat.kohli@mycsu.edu> | DATA200 | A (97)
Harmanpreet Kaur <harmanpreet.kaur@mycsu.edu> | CS101 | B+ (88)
Rohit Sharma <rohit.sharma@mycsu.edu> | CS101 | B (84)
Mithali Raj <mithali.raj@mycsu.edu> | STAT150 | A- (91)
```

---

## 🧠 Design Highlights

* Uses **Python lists (arrays)** to meet data structure requirements
* All CRUD operations persist automatically to CSV
* Measures execution times with `perf_counter()`
* Unit tests validate encryption, persistence, sorting, and CRUD correctness
* Safe handling for missing/invalid CSV headers

---

## 🧪 Run Unit Tests

```bash
python checkmygrade.py -m tests
```

Outputs include:

* Encryption/login validation
* CRUD test results
* Sorting & search timings for 1000 generated students


---

## 📜 License

This project is licensed under the **MIT License** — feel free to use and modify it for learning or academic purposes.

---

## 🌟 Credits

Built by **SIVA SURYA CHANDRAN** for the *CheckMyGrade* lab assignment.
Inspired by the concept of minimal data-driven educational systems.

---

