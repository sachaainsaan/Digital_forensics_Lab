# Experiment 08 — Steganography

**Aim:**  
To perform steganographic analysis on digital images using StegExpose and OpenStego tools, detect hidden information, and extract the concealed data for forensic examination.

---

## Tools Used
- **Tool :** StegExpose (Java-based Detection Tool)  
- **Version:** 0.2  
- **Operating System:** Windows 11             
- **File Types:** `.jpg`, `.png`, `.bmp`  
- **Output Type:** Hidden file (e.g., `.txt`, `.zip`)

---

## Procedure 
1. Opened **Command Prompt** in the folder containing StegExpose.  
2. Ran the following command to analyze images:
3. StegExpose scanned all images in the specified directory and generated a report (`steganalysis.csv`).  
4. Checked the CSV file for **Suspiciousness Scores** (values > 0.2 indicated likely stego images).  
5. Verified that `image_stego.png` had a high suspicion score, confirming hidden data presence.

---

## Result / Observation
The experiment successfully demonstrated both **steganography** and **steganalysis** (data detection).  
OpenStego was used to embed and extract hidden data from an image, while StegExpose successfully detected the stego file through statistical analysis.

---

## Conclusion
The experiment demonstrates the use of **StegExpose** for practical steganography analysis.  
While OpenStego helps conceal and recover hidden data, StegExpose is valuable for forensic investigators to detect steganographic content and identify suspicious digital files.

---

## Viva / Important Questions

1. **What is Steganography?**  
→ The practice of hiding secret information within another file, such as an image, video, or audio.

2. **How is Steganography different from Cryptography?**  
→ Cryptography hides the *content* of a message, while steganography hides the *existence* of the message itself.

3. **What are common file types used for steganography?**  
→ Image, Audio, Video, and Document files.

4. **What is StegExpose used for?**  
→ It’s a steganalysis tool that detects hidden data in image files based on statistical features.

5. **What indicates that an image might contain hidden data?**  
→ A higher suspiciousness score in analysis tools or increased file size compared to the original.

6. **Why is steganography analysis important in digital forensics?**  
→ To uncover hidden communication, exfiltrated data, or evidence concealed in multimedia files.
