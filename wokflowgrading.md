# Student Grading & Information Management System — Evidence & Documentation

This repository serves as complete evidence for the implementation and testing of the **Student Grading & Information Management System** developed in C.

---

## 📌 Task Evidence & Test Results

### Task 5: Interactive Student Data Entry & Grade Evaluation
- **File:** `task5.c`
- **Objective:** Accept user input for student details (Registration Number, Name, Marks) and calculate the appropriate letter grade based on conditional ranges.

#### Implementation & Execution Evidence
![Task 5 Execution](/grading/gradeone.png)

```c
// Key Logic Snippet (task5.c)
int main() {
    int reg_no;
    char name[50];
    float marks;
    char grade;

    printf("Enter Registration Number: ");
    scanf("%d", &reg_no);
    printf("Enter Name: ");
    scanf("%s", name);
    printf("Enter Marks: ");
    scanf("%f", &marks);

    if (marks >= 70 && marks <= 100) {
        grade = 'A';
    } else if (marks >= 60 && marks < 70) {
        grade = 'B';
    }
    // ...
}
```

---

### Task 6: Formatted Student Information Display
- **File:** `task6.c`
- **Objective:** Format and output student credentials into a structured report card layout in the terminal using formatted string output.

#### Implementation & Execution Evidence
![Task 6 Execution](/grading/gradingout.png)

```
----------------------------------
       STUDENT INFORMATION
----------------------------------
Registration No: 890
Name: Max
Marks: 85
Grade: A
----------------------------------
```

---

### Task 7: Batch Processing & Pass/Fail Evaluation Loop
- **File:** `task7.c`
- **Objective:** Iterate over `N` student records dynamically, prompt for input, evaluate pass/fail criteria (`marks >= 40`), and print summary lines.

#### Implementation & Execution Evidence
![Task 7 Execution](/grading/pass.png)

```c
// Key Logic Snippet (task7.c)
int main() {
    int N, i;
    printf("Enter the number of students: ");
    scanf("%d", &N);

    for (i = 0; i < N; i++) {
        int reg_no, marks;
        char name[50];

        printf("Enter registration number: ");
        scanf("%d", &reg_no);
        printf("Enter name: ");
        scanf("%s", name);
        printf("Enter marks: ");
        scanf("%d", &marks);

        if (marks >= 40) {
            // Pass logic output...
        }
    }
}
```

---

### Task 8: Dual Grading Logic (`if-else` vs `switch-case`)
- **File:** `task8.c`
- **Objective:** Implement and verify two distinct evaluation methods (`if-else` vs `switch-case`) side-by-side to ensure logic consistency.

#### Implementation & Execution Evidence
![Task 8 Execution](/grading/final.png)

```
Enter the student's score: 89
Using if-else if-else:
Grade: B
Using switch-case:
Grade: B
```

---

## 🛠️ How to Compile and Run

### Using GCC Compiler (Terminal)
```bash
# Compile and run any specific task file
gcc task5.c -o task5
./task5

gcc task8.c -o task8
./task8
```

### Using Code::Blocks IDE
1. Open `Assignments.cbp`.
2. Select the target file (`task5.c`, `task6.c`, `task7.c`, or `task8.c`).
3. Press **F9** (or click **Build and Run**).

---


```
