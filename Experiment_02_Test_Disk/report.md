# Experiment 02 — TestDisk

**Aim:**  
To recover deleted or lost partitions and files using the TestDisk forensic tool and analyze the recovered data.

---

## Tools Used
- **Tool Name:** TestDisk  
- **Version:** 7.3  
- **Operating System:** Windows 11
- **Image / File Type:** Disk Image   

---

## Procedure
1. Launched **TestDisk** 
2. Selected **Create a New Log File** to record all recovery operations.  
3. Chose the **disk or image file** to analyze 
4. Selected the partition table type — automatically detected as **Intel/PC partition**.  
5. Chose the **Analyse** option to scan for lost partitions.  
6. TestDisk displayed the **current partitions** and started a **Quick Search**.  
7. Identified the deleted/lost partitions shown in red.  
8. Performed a **Deeper Search** to ensure all possible partitions were found.  
9. Verified the partitions to confirm correctness by checking file listings.  
10. Pressed **P** to preview files within each recovered partition.  
11. Selected the desired partition and used the **Write** option to restore it.  
12. Saved the restored partition table and exited the program.  
13. Rebooted the system (if required) to check that the partition appeared again in File Explorer.  

---

## Result / Observation
The **TestDisk** utility successfully detected and recovered deleted partitions from the given disk image.  
Recovered partitions were accessible after recovery, and files were verified to be intact and readable.  

---

## Conclusion
This experiment demonstrates the use of **TestDisk** for forensic partition recovery.  
The tool effectively analyzes disk structures, detects lost or corrupted partitions, and recovers them without data modification — ensuring forensic accuracy in recovery procedures.

---

## Viva / Important Questions

1. **What is the primary use of TestDisk?**  
→ TestDisk is used to recover lost partitions and make non-booting disks bootable again.

2. **What is the difference between Quick Search and Deeper Search?**  
→ Quick Search scans for recently deleted partitions, while Deeper Search performs a sector-by-sector analysis for older or corrupted partitions.

3. **Can TestDisk recover individual files?**  
→ Yes, TestDisk allows browsing lost partitions and copying individual files to a safe location.

4. **Why is partition recovery important in digital forensics?**  
→ It helps investigators retrieve hidden or deleted evidence stored in lost partitions.

5. **Is TestDisk a GUI or CLI tool?**  
→ TestDisk is primarily a Command-Line Interface (CLI) tool, which ensures better control and precision for forensic analysis.

