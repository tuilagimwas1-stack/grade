# Student Grading & Information Management System (C Implementation)

A C-based console application suite designed for managing student records, calculating letter grades using conditional logic (`if-else` and `switch-case`), evaluating pass/fail statuses, and iterating over multiple student entries.

---

## 📚 Tasks Overview

### Task 5: Interactive Student Data Entry & Grade Evaluation
* **File:** `task5.c`
* **Description:** Prompts user input for student details (Registration Number, Name, Marks) and evaluates the letter grade based on predefined mark ranges.
* **Grading Scale:**
  * `70 - 100` : **Grade A**
  * `60 - 69`  : **Grade B**
  * `50 - 59`  : **Grade C**
  * *(and so on...)*

#### Implementation Snippet (`task5.c`):
```c
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
    } ...
}
```

---

### Task 6: Static Student Information Display
* **File:** `task6.c`
* **Description:** Formats and outputs student details into a structured card/report format in the terminal using formatted `printf` statements.

#### Sample Console Output:
```text
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

### Task 7: Batch Student Processing & Pass/Fail Status
* **File:** `task7.c`
* **Description:** Uses a loop to process `N` number of students. Checks whether each student meets the passing threshold (e.g., `marks >= 40`) and outputs their grade and pass/fail status.

#### Implementation Snippet (`task7.c`):
```c
int main() {
    int N, i;
    printf("Enter the number of students: ");
    scanf("%d", &N);

    for (i = 0; i < N; i++) {
        int reg_no, marks;
        char name[50];
        char grade;

        printf("Enter registration number: ");
        scanf("%d", &reg_no);
        printf("Enter name: ");
        scanf("%s", name);
        printf("Enter marks: ");
        scanf("%d", &marks);

        if (marks >= 40) {
            // Pass logic...
        }
    }
}
```

---

### Task 8: Dual-Method Grading (`if-else` vs `switch-case`)
* **File:** `task8.c`
* **Description:** Implements and compares two distinct function-based approaches for determining student letter grades given a numerical score:
  1. `grading_if_else(score)` — Uses standard conditional branching.
  2. `grading_switch_case(score)` — Uses integer division mapping (e.g., `score / 10`) to perform `switch-case` evaluation.

#### Sample Execution:
```text
Enter the student's score: 89
Using if-else if-else:
Grade: B
Using switch-case:
Grade: B
```

---

## 🛠️ How to Compile & Run

### Using GCC Compiler via Terminal:
```bash
# Compile any task individually
gcc task5.c -o task5
./task5

gcc task8.c -o task8
./task8
```

### Using Code::Blocks IDE:
1. Open the project workspace `Assignments.cbp`.
2. Select the target task C file (`task5.c`, `task6.c`, `task7.c`, or `task8.c`).
3. Press `F9` (or click **Build and Run**).

---

## 📁 Repository Structure

```text
.
├── main.c
├── task1.c
├── task2.c
├── task3.c
├── task4.c
├── task5.c   # Interactive data entry & grade classification
├── task6.c   # Formatted student information card output
├── task7.c   # Multi-student loop with pass/fail evaluation
└── task8.c   # Dual grading comparison (if-else vs switch-case)
```
