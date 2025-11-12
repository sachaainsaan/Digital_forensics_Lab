# Experiment 09 — Process Explorer (Malware Detection and Process Analysis)

**Aim:**  
To inspect running processes using Process Explorer, identify unknown or high CPU-usage processes, verify them using VirusTotal, and terminate any suspicious or malicious activity.

---

## Tools Used
- **Tool Name:** Process Explorer
- **Version:** v17.06  
- **Operating System:** Windows 11  
- **File Type:** Executable 
- **Purpose:** Real-time process monitoring and malware detection  

---

## Procedure 
1. Downloaded **Process Explorer** from the official Microsoft Sysinternals website.  
2. Extracted the zip folder and launched the executable file:
3. The **Process Explorer dashboard** displayed a hierarchical view of all running processes.  
4. Sorted processes by **CPU usage** to identify any process consuming unusually high resources.  
5. Noted down suspicious processes showing:  
- Unusual names
- No company signature  
- Unknown or blank description fields  
6. Right-clicked on the suspicious process → **Properties** to view detailed metadata:  
- Image path  
- Command line  
- Digital signature status  
- Threads, handles, and DLLs  
7. Verified the file’s signature:  
- Right-click → **Verify Image**  
- Checked if it was **digitally signed by Microsoft / known vendor**  
8. If the process was unsigned or suspicious, copied the **file path** from the properties window.  
9. Opened the file location via:  
- Right-click → **Open File Location**  
10. Uploaded the suspicious executable to **VirusTotal** (https://www.virustotal.com).  
11. Observed the scan results from multiple antivirus engines.  
- If VirusTotal reported **“Malicious” or “Suspicious”**, marked it as potentially harmful.  
12. Returned to Process Explorer and right-clicked the malicious process → **Kill Process** (or “Kill Process Tree”).  
13. Re-verified CPU usage and system performance after termination — ensured normal activity resumed.  
14. Recorded all findings, including process details, VirusTotal report, and actions taken.

---


## Result / Observation
The analysis successfully identified a high CPU-consuming, unsigned process.  
VirusTotal confirmed the executable was malicious.  
The process was safely terminated through Process Explorer, restoring normal CPU performance and ensuring system security.

---

## Conclusion
The experiment demonstrates the use of **Process Explorer** for forensic process inspection and malware detection.  
It helps investigators identify abnormal resource usage, verify suspicious executables through VirusTotal, and terminate malicious processes effectively.  
Process Explorer is a vital tool for live forensic investigations and malware response.

---

## Viva / Important Questions

1. **What is Process Explorer used for?**  
→ To monitor, analyze, and manage running processes, detect anomalies, and inspect detailed resource usage.

2. **How can CPU usage indicate malware activity?**  
→ Malware often consumes high CPU or memory resources without user initiation.

3. **Why is VirusTotal used in process analysis?**  
→ It scans suspicious files with multiple antivirus engines to confirm if the file is malicious.

4. **What are signs of a suspicious process?**  
→ Unknown name, no digital signature, high CPU usage, unusual file location.

5. **How can you terminate a malicious process safely?**  
→ Right-click the process in Process Explorer → “Kill Process” or “Kill Process Tree.”

6. **What is the difference between “Kill Process” and “Kill Process Tree”?**  
→ “Kill Process” stops only the selected process; “Kill Process Tree” stops that process and all its child processes.
