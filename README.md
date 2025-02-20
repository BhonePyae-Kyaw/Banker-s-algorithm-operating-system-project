# 🚀 Banker's Algorithm - Operating System Project  

This is a **Python implementation of the Banker's Algorithm**, designed for an **Operating Systems** class. The algorithm determines whether a system is in a **safe state** by simulating resource allocation among processes.

## 📌 Features  
- Reads input from a **.txt file** containing:  
  - **Maximum Matrix** (Maximum resource demand per process)  
  - **Allocated Matrix** (Current allocated resources per process)  
  - **Resources** (Total system resources)  
- Displays **step-by-step execution** with four matrices:  
  - **Available Resources**  
  - **Allocated Matrix**  
  - **Maximum Matrix**  
  - **Need Matrix**  
- Determines if the system is in a **safe state**:  
  - ✅ If **safe**, prints the **safe sequence** (order of process execution).  
  - ❌ If **not safe**, prints only the processes that were executed before a deadlock occurs.  

## 🛠 How It Works  
1. The algorithm reads the resource allocation details from a `.txt` file.  
2. It calculates the **Need Matrix**:  
   \[
   \text{Need} = \text{Maximum} - \text{Allocated}
   \]
3. The system iteratively checks if any process can safely execute given the **available resources**.  
4. If a process executes, its allocated resources are released and added to the **available resources**.  
5. The process continues until either:  
   - All processes execute (**safe state**)  
   - No further processes can execute (**unsafe state / deadlock**)  

## 📂 Input File Format  
The `.txt` file should be structured as follows:  
```
# Maximum Matrix (P0, P1, P2, ...)
7 5 3
3 2 2
9 0 2
2 2 2
4 3 3

# Allocated Matrix
0 1 0
2 0 0
3 0 2
2 1 1
0 0 2

# Resources
3 3 2
```

## 📌 Example Output  
```
==================================================
Available Resources: [3, 3, 2]
Allocation Matrix:
[[0, 1, 0], [2, 0, 0], [3, 0, 2], [2, 1, 1], [0, 0, 2]]
Maximum Matrix:
[[7, 5, 3], [3, 2, 2], [9, 0, 2], [2, 2, 2], [4, 3, 3]]
Need Matrix:
[[7, 4, 3], [1, 2, 2], [6, 0, 0], [0, 1, 1], [4, 3, 1]]
==================================================

✅ It is a safe sequence.
The safe sequence is < P0 P1 P2 P3 P4 >
```

## 📌 Future Improvements  
🔹 Support for **dynamic user input** instead of file input.  
🔹 GUI-based visualization of resource allocation.  
🔹 Support for **multithreading** to simulate real-time execution.  

---

### 🎯 **Contributions & Feedback**  
Feel free to **fork**, **contribute**, or **suggest improvements**! If you find any bugs or have ideas for enhancements, open an **issue** or submit a **pull request**.  

🚀 Happy Coding! 😊
