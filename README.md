# 🚀 Banker's Algorithm - Operating System Project  

This is a **Python implementation of the Banker's Algorithm**, designed for an **Operating Systems** class. The algorithm determines whether a system is in a **safe state** by simulating resource allocation among processes.

## 📌 Features  
- Reads input from a **.txt file** containing:  
  - **Maximum Matrix** (Maximum resource demand per process)  
  - **Allocated Matrix** (Current allocated resources per process)  
  - **Available Resources** (Total system resources)  
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

# Available Resources
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

Executing process: P1
Executing process: P3
Executing process: P4
Executing process: P2
Executing process: P0

✅ Safe Sequence Found: < P1 P3 P4 P2 P0 >
```

## 🚀 How to Run  
1. Clone the repository:  
   ```sh
   git clone https://github.com/yourusername/Bankers-Algorithm.git
   cd Bankers-Algorithm
   ```
2. Place the input `.txt` file in the project directory.  
3. Run the script:  
   ```sh
   python bankers_algorithm.py
   ```
4. Follow the prompts and enter the file name when requested.  

## 📌 Requirements  
- Python 3.x  

## 📌 Future Improvements  
🔹 Support for **dynamic user input** instead of file input.  
🔹 GUI-based visualization of resource allocation.  
🔹 Support for **multithreading** to simulate real-time execution.  

---

### 🎯 **Contributions & Feedback**  
Feel free to **fork**, **contribute**, or **suggest improvements**! If you find any bugs or have ideas for enhancements, open an **issue** or submit a **pull request**.  

🚀 Happy Coding! 😊
