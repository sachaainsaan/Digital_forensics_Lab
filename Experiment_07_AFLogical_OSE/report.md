# Experiment 07 — AFLogical OSE (Android Forensics)

**Aim:**  
To acquire and analyze logical data from an Android smartphone using AFLogical OSE and extract information such as call logs, contacts, messages, and application data.

---

## Tools Used
- **Tool Name:** AFLogical OSE (Open Source Edition)  
- **Version:** 1.6.3  
- **Operating System:** Windows 10 / Linux 
- **Mobile Platform:** Android OS  
- **Connection Type:** USB Debugging via ADB   
- **Output Type:** `.zip` archive containing CSV data files

---

## Procedure (Step-by-Step)
1. Installed **AFLogical OSE** on the system.  
   - Tool can be downloaded from **AFLogical OSE GitHub Repository**.  
2. Enabled **Developer Options** on the Android device.  
   - Go to *Settings → About Phone → Tap “Build Number” seven times*.  
3. Enabled **USB Debugging** on the phone:  
   - *Settings → Developer Options → USB Debugging → ON*  
4. Connected the Android phone to the system via USB cable.  
5. Verified the connection using:
→ Displayed the connected device ID.  
6. Launched **AFLogical OSE** from the terminal or command prompt.  
- On Windows: `AFLogical OSE.exe`  
- On Linux: `java -jar AFLogical-OSE.jar`
7. On the mobile device, a **Superuser / Root permission** prompt appeared — tapped **Grant Access**.  
8. Selected data types to extract:  
- Contacts  
- Call Logs  
- SMS / MMS  
- Calendar Events  
- Installed Applications  
9. AFLogical OSE performed logical acquisition and stored results on the SD card (or internal storage) in a folder named:
10. Copied the generated `.zip` file from the mobile device to the PC using:
 ```
 adb pull /sdcard/forensics/AFLogical-YYYYMMDD-HHMMSS.zip
 ```
11. Extracted the `.zip` archive to view multiple `.csv` files containing:
 - contacts.csv  
 - sms.csv  
 - calllogs.csv  
 - calendar.csv  
12. Opened the CSV files in Excel to examine extracted data such as timestamps, numbers, and messages.

---


## Result / Observation
AFLogical OSE successfully performed a **logical acquisition** of the connected Android device.  
It extracted essential forensic artifacts such as call logs, contacts, SMS messages, and calendar entries in CSV format without altering the original data.

---

## Conclusion
The experiment demonstrates how **AFLogical OSE** is used for **mobile device forensics**, specifically for logical data acquisition.  
It provides an efficient and non-intrusive way to extract user data from Android devices, ensuring data integrity and admissibility as digital evidence.

---

## Viva / Important Questions

1. **What is AFLogical OSE?**  
→ It is an open-source mobile forensic tool for logical data acquisition from Android devices.

2. **What is the difference between logical and physical acquisition?**  
→ Logical acquisition extracts user-accessible data, while physical acquisition copies the entire memory (including deleted or hidden files).

3. **What data can AFLogical OSE extract?**  
→ Contacts, call logs, SMS, MMS, calendar, and installed app information.

4. **Why is USB Debugging required?**  
→ It allows the forensic tool to communicate with the Android device via ADB commands.

5. **What is the output format of AFLogical OSE?**  
→ The tool exports data as a `.zip` archive containing `.csv` reports.

6. **Can AFLogical OSE work without root access?**  
→ It can perform limited logical acquisition without root; full data extraction requires root permissions.
