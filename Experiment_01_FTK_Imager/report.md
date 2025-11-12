# Experiment 01 — FTK Imager

**Aim:**  
To acquire a forensic image of a disk or folder using FTK Imager and verify its integrity through hash verification.

---

## Tools Used
- **Tool Name:** FTK Imager  
- **Version:** 4.3 AccessData FTK Imager  
- **Operating System:** Windows 10 (64-bit)  
- **Image Type:** Logical image  
- **Hash Algorithms:** MD5, SHA1  

---

## Procedure (Step-by-Step)
1. Launched **FTK Imager** on the system.  
2. Clicked on **File → Create Disk Image**.  
3. In the *Select Source* window, chose **Contents of a Folder** (since only one physical drive was available).  
4. Selected the source folder:
5. Selected the destination folder for saving the image:  
6. Chose the image type as **E01 (EnCase Image Format)**.
7. Entered case details:  
- **Case Number:** 01  
- **Evidence Number:** 001  
- **Examiner:** Venkatesh J 
- **Description:** Logical image of a folder for forensic analysis.  
8. Set **image fragment size** to 600 MB (default).  
9. Clicked **Start** to begin the imaging process.  
10. Waited for FTK Imager to complete imaging and generate **MD5 and SHA1 hashes**.  
11. Verified that both hashes matched during post-acquisition verification.  

---

## Result / Observation
The logical image of the target folder was successfully created using FTK Imager.  
The MD5 and SHA1 hash values generated before and after imaging were identical, confirming the integrity of the evidence.  

---

## Conclusion
The experiment demonstrates the use of FTK Imager for creating forensic disk or folder images in `.E01` format.  
The process also verifies data integrity using cryptographic hashing, ensuring that no data modification occurred during acquisition.  

---

## Viva / Important Questions

1. **What is FTK Imager used for?**  
→ It is used to acquire, preview, and verify forensic images of disks, partitions, or folders.

2. **What is the significance of hashing in digital forensics?**  
→ Hashing ensures data integrity by verifying that the evidence has not been altered.

3. **What is the difference between logical and physical imaging?**  
→ Logical imaging captures files and folders; physical imaging captures the entire storage, including deleted data and slack space.

4. **Why can’t we store the disk image on the same drive being imaged?**  
→ It risks overwriting the source data and invalidating evidence integrity.

5. **What is the `.E01` format?**  
→ It’s the EnCase forensic image format that supports metadata, compression, and embedded hash verification.


