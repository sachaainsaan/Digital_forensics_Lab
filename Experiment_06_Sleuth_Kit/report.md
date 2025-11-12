# Experiment 06 — Sleuth Kit (TSK)

**Aim:**  
To perform forensic analysis of a disk image using the command-line tools of The Sleuth Kit (TSK) to extract metadata, list partitions, and recover deleted files.

---

## Tools Used
- **Tool Name:** The Sleuth Kit (TSK)  
- **Version:** 4.14.0  
- **Operating System:** Windows 10 (using Command Prompt)  
- **File Type:** Forensic disk image (`.E01` / `.dd` / `.img`)  
- **Supported File Systems:** FAT, NTFS, EXT, HFS, ISO9660  

---

## Procedure (Step-by-Step)
1. Installed **Sleuth Kit** on the system.  
   - Windows: Extracted and added the Sleuth Kit folder to the PATH environment.  
   - Linux: Installed using `sudo apt install sleuthkit`.  
2. Opened **Command Prompt** (or Terminal) and navigated to the Sleuth Kit `bin` directory.  
3. Loaded a forensic image file for analysis:  
- The `-o 63` option specifies the partition offset.
4. Used **mmls** to list partition details:  
→ Displayed partition start sectors, types, and lengths.
5. Identified the partition offset and used **fsstat** to get filesystem metadata:  
→ Displayed file system type, sector size, and last mount time.
6. Listed root directory files using **fls**:  
→ Displayed deleted and active file entries with inode numbers.
7. Extracted a deleted file using **icat**:  
→ Extracted file from inode 128 to a new file `recovered.txt`.
8. Verified the recovered file’s hash to ensure data integrity using `md5sum`:  
9. Documented all command outputs and results for analysis.

---


## Result / Observation
The Sleuth Kit successfully identified the file system structure and recovered deleted files from the given forensic image using command-line analysis.  
The recovered files’ hash values matched the originals, ensuring data integrity and authenticity of evidence.

---

## Conclusion
This experiment demonstrates the use of **The Sleuth Kit (TSK)** for low-level forensic analysis of disk images.  
It provides investigators with the ability to extract partitions, list file metadata, recover deleted content, and perform integrity checks entirely from the command line — making it a powerful open-source forensic framework.

---

## Viva / Important Questions

1. **What is Sleuth Kit used for?**  
→ Sleuth Kit is a collection of command-line tools for digital forensic analysis of disks and file systems.

2. **Name some tools included in Sleuth Kit.**  
→ `mmls`, `fsstat`, `fls`, `icat`, `istat`, `img_stat`.

3. **What is the function of `mmls`?**  
→ It lists the partition layout of a forensic image.

4. **What does the `icat` command do?**  
→ It extracts the content of a file from a disk image using its inode number.

5. **Why is Sleuth Kit important in forensics?**  
→ It provides detailed access to file systems and metadata, allowing precise recovery and verification of evidence.

