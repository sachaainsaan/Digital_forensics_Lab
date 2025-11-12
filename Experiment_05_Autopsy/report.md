# Experiment 05 — Autopsy

**Aim:**  
To analyze a forensic disk image using Autopsy and recover deleted or hidden files, identify user activity, and generate an investigation report.

---

## Tools Used
- **Tool Name:** Autopsy  
- **Version:** 4.22.1 
- **Operating System:** Windows 10 (64-bit)  
- **Image Type:** Forensic disk image (`.E01`)  
- **Hash Algorithm:** MD5, SHA1 (for integrity verification)

---

## Procedure (Step-by-Step)
1. Launched **Autopsy** on the system.  
2. Selected **Create New Case** and provided the following details:  
   - Case Name:
   - Base Directory: 
3. Clicked **Next → Add Data Source → Disk Image or VM File**.  
4. Selected the forensic image file (e.g., `Documents_Image.E01` or `sample_disk.dd`).  
5. Autopsy automatically detected the file system type (e.g., NTFS or FAT32).  
6. Selected **Ingest Modules** to process the evidence:  
   - File Type Identification  
   - Keyword Search  
   - Hash Lookup  
   - Extract Web History  
   - Deleted Files Analysis  
7. Clicked **Next → Finish** to start ingesting the data.  
8. Waited for the processing to complete  
9. Navigated to **Tree View → Data Sources** to explore:  
   - File System  
   - Deleted Files  
   - Web History  
   - Recent Documents  
10. Examined recovered files and double-clicked to preview their contents.  
11. Checked **Reports → HTML / CSV** to generate an investigation report summarizing findings.  
12. Verified MD5 hash of the source image to ensure data integrity was maintained.  

---


## Result / Observation
Autopsy successfully analyzed the forensic image and recovered deleted files, browser activity, and user document trails.  
It also generated a structured investigation report containing file metadata, timestamps, and activity logs, confirming the forensic workflow’s effectiveness.

---

## Conclusion
The experiment demonstrates how **Autopsy** aids in digital evidence analysis and recovery.  
It automates the investigation of disk images, identifies deleted and hidden files, and extracts useful evidence like browsing history and user artifacts.  
Autopsy is one of the most powerful tools used in real-world forensic investigations.

---

## Viva / Important Questions

1. **What is Autopsy used for?**  
→ Autopsy is used for analyzing forensic disk images to recover deleted files and extract digital evidence.

2. **What is the difference between Autopsy and FTK Imager?**  
→ FTK Imager is used for acquiring forensic images, while Autopsy is used for analyzing them.

3. **What are Ingest Modules in Autopsy?**  
→ They are built-in modules that automate analysis tasks like keyword search, hash lookup, and web history extraction.

4. **Why is hash verification important in Autopsy?**  
→ It ensures the evidence integrity is maintained — no data alteration during analysis.

5. **What types of evidence can Autopsy extract?**  
→ Deleted files, email data, browser history, recently accessed files, user accounts, and system logs.
