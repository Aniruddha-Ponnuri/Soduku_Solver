# 🧩 Sudoku Solver (C++)

## 📖 Overview
This **Sudoku Solver** is a console-based C++ program that takes in an unsolved Sudoku puzzle and computes its solution using a **recursive backtracking algorithm**.

It guides the user through inputting puzzle values manually, solves the grid, and displays the completed Sudoku with clear formatting and color separation between subgrids.

---

## ⚙️ Features
- ✅ **Interactive input:** Prompts the user to enter Sudoku values (0 for empty cells).  
- 🔍 **Validation checks:** Ensures only valid numbers (0–9) are accepted.  
- 🧠 **Backtracking algorithm:** Efficiently finds the correct solution using recursion.  
- 🧾 **Editable cell tracking:** Differentiates between fixed and editable cells.  
- 🎨 **Formatted output:** Displays the Sudoku board neatly in a colored grid layout.  
- 📊 **Recursion stats (optional):** Tracks how many recursive calls were made.

---

## 🧩 How It Works
1. **Input Phase:**  
   - The program asks you to fill in each cell of the Sudoku grid (9×9).  
   - Enter `0` for empty cells.  
   - Invalid inputs are rejected until corrected.

2. **Solving Phase:**  
   - The solver calculates possible numbers for each cell using Sudoku rules:
     - No duplicate numbers in any **row**, **column**, or **3×3 subgrid**.
   - It recursively tries valid numbers until the board is complete.

3. **Output Phase:**  
   - Displays the solved Sudoku grid in a formatted layout.  
   - Optionally, prints recursion statistics.

---

## 🧠 Core Components

### **1. SudokuFrame Class**
Handles:
- Reading puzzle input  
- Tracking editable vs fixed cells  
- Displaying the Sudoku grid  
- Clearing cells during backtracking  

### **2. Possibilities Class**
Implements a simple linked-list structure to store possible valid numbers for each cell.

### **3. SudokuSolver Class**
Coordinates the solving process:
- Uses **backtracking** to test valid numbers recursively.  
- Calls validation functions for rows, columns, and subgrids.  
- Tracks recursion count for performance insight.

---

## 🖥️ Example Usage

### 🧮 Input:
```
Welcome to Sudoku Solver!
Before we start, you will have to input the puzzle into this program.

Enter the specified value when prompted.
Enter 0 if cell is empty.

Enter value for cell[1][1] --> 5
Enter value for cell[1][2] --> 3
Enter value for cell[1][3] --> 0
...
```

### ✅ Output:
```
++=====================================++
|| 5  3  4 || 6  7  8 || 9  1  2 ||
++-----------++-----------++-----------++
|| 6  7  2 || 1  9  5 || 3  4  8 ||
...
++=====================================++

QED. Your puzzle has been solved!
```

---

## 🧩 Algorithm Summary

The solver uses a **recursive backtracking** approach:
1. Start from the top-left cell.
2. Find all possible valid numbers for the cell.
3. Place a number and move to the next cell.
4. If a dead end is reached, **backtrack** — reset the cell and try the next possibility.
5. Continue until the board is fully filled.

---

## 🧾 Compilation & Execution

### **Compile:**
```bash
g++ sudoku_solver.cpp -o sudoku_solver
```

### **Run:**
```bash
./sudoku_solver
```

---

## 📁 File Structure
```
.
├── sudoku_solver.cpp   # Main program file
└── README.md           # Documentation (this file)
```

---


