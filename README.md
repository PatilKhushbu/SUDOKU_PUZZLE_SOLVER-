# 🧩 Sudoku Puzzle Solver  

**An intelligent Sudoku puzzle solver implementing constraint propagation and backtracking algorithms.**  

---

## 📌 Overview  
This project solves standard 9×9 Sudoku puzzles using **Artificial Intelligence** techniques:  
- **Constraint Propagation (AC-3 Algorithm)**  
- **Forward Checking**  
- **Backtracking Search with Heuristics (MRV & LCV)**  

It ensures correctness while optimizing performance through domain reduction and intelligent search strategies.  

---

## 🚀 Features  

### 🔗 **Constraint Propagation (AC-3)**  
- Transforms high-order `Alldiff` constraints into binary constraints.  
- Enforces arc consistency before search, reducing variable domains.  

### 🔍 **Forward Checking**  
- Dynamically prunes invalid values from neighboring cells during search.  
- Prevents early dead-ends by maintaining consistency.  

### ↩️ **Backtracking with Heuristics**  
- **MRV (Minimum Remaining Values)**: Chooses the variable with the fewest legal moves.  
- **LCV (Least Constraining Value)**: Prefers values that restrict other variables the least.  

### 📊 **Efficiency Optimizations**  
- Recursive depth-first search with pruning.  
- State backtracking to undo invalid assignments.  

---

## 🛠️ Implementation  

### 📂 **Code Structure**  
| File | Description |  
|------|-------------|  
| `AC3.java` | Enforces arc consistency using AC-3 algorithm. |  
| `Backtracking.java` | Solves Sudoku using backtracking + forward checking. |  
| `Node.java` | Represents a Sudoku cell (domain, constraints). |  
| `Test.java` | Runs tests with optional verbose logging. |  

### ▶️ **How to Run**  
1. **Input Format**:  
   - Represent the Sudoku grid as a 9×9 matrix.  
   - Use `0` or blanks for empty cells.  

2. **Execution**:  
   - **AC-3 Only**:  
     ```java
     new AC3(Node.getNodes("puzzle_data"));
     ```
   - **Full Solver (Backtracking + Forward Checking)**:  
     ```java
     new Backtracking(Node.getNodes("puzzle_data"));
     ```

3. **Verbose Mode**:  
   - Enable detailed step logs in `Test.java`:  
     ```java
     Test.VERBOSE = true;
     ```

---

## 📊 **Example Output**  
### **Input Puzzle**  
```
[0][7][0][8][0][0][0][0][0]  
[2][0][0][3][0][6][0][7][0]  
[0][9][8][0][2][0][1][3][0]  
... (remaining rows)
```
### **Solved Grid**  
```
[9][7][3][5][8][4][6][2][1]  
[8][2][4][9][1][6][5][3][7]  
[1][6][5][7][2][3][8][9][4]  
... (full solution)
```

---

## 📝 **Conclusion**  
- **AC-3 + Forward Checking** ensures efficient domain reduction.  
- **Backtracking with MRV & LCV** minimizes search time.  
- The solver handles even complex puzzles with optimal performance.  

For debugging, use `VERBOSE` mode to track each step!  

---

## 👥 **Contributors**  
- **Patil Khushbu Mahendra** (882697)  
- **Khalid Vafa** (882677)  

---

**🎯 Happy Solving!** 🧠⚡
