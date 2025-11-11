
#  Ex.No.2    TestDisk: Open-Source Data Recovery Tool

## Aim :
To use TestDisk step by step to recover a missing partition and repair a corrupted one.



## 🛠️ Installation
Linux (Debian/Ubuntu): sudo apt-get install testdisk

macOS (Homebrew): brew install testdisk

Windows: Download the executable from the official CGSecurity website.

## Procedure

### 1. Create a Log File
- Launch TestDisk from your terminal or command prompt using sudo testdisk (or testdisk_win.exe on Windows).

- Select the [Create] option to generate a log file of the recovery session. This is helpful for future reference or troubleshooting.
<br>
<br>

<img width="1098" height="629" alt="Screenshot 2025-09-02 152816" src="https://github.com/user-attachments/assets/d6b20b59-0f83-43ab-b9ae-205149141def" />


</p>
<br>
<br>

### 2. Select the Drive to Analyze
- TestDisk will display a list of all detected storage devices.

- Use the Up/Down arrow keys to highlight the drive that contains your lost data.

<br>
<br>

<img width="1099" height="629" alt="Screenshot 2025-09-02 152428" src="https://github.com/user-attachments/assets/5ffa9691-5240-4005-a0be-d74a8829acd6" />



</p>
<br>
<br>

- Select [Proceed] to move to the next step.

### 3. Choose the Partition Table Type
- TestDisk will automatically suggest the most likely partition table type (e.g., Intel/PC, EFI GPT).

- The default value is usually correct. Confirm the selection by pressing Enter.
<br>
<br>
<img width="1100" height="609" alt="Screenshot 2025-09-02 152452" src="https://github.com/user-attachments/assets/61f28ffb-1151-41a3-8dd7-4981d94b6828" />


</p>
<br>
<br>

### 4. Analyze Current Partition Structure
- From the main menu, choose [Analyse] and press Enter.
<br>
<br>
<img width="1090" height="602" alt="Screenshot 2025-09-02 152504" src="https://github.com/user-attachments/assets/6ddf3da6-6dd9-4a7c-bd8b-96c46358f823" />



</p>
<br>
<br>

- This will display the current partition table and check for errors or missing partitions.

### 5. Perform a Quick Search
- After the analysis, you will be prompted to perform a [Quick Search].

<br>
<br>
<img width="1094" height="640" alt="Screenshot 2025-09-02 152535" src="https://github.com/user-attachments/assets/382d258a-5f75-4893-afe6-13281e5d8e12" />




</p>
<br>
<br>

- Select it and press Enter to scan the drive for lost partitions.

- Once a partition is found, you can press p to list its files. Deleted files and folders often appear in red.

- Press q to return to the search results.

  ### 6. Perform a Deeper Search
- If the Quick Search fails to find your lost partitions, select [Deeper Search].

-<br>
<br>
<img width="1103" height="633" alt="Screenshot 2025-09-02 154528" src="https://github.com/user-attachments/assets/55b45c4c-cd63-4dde-9695-150967ec3741" />



</p>
<br>
<br>

- This process can take a long time, as it scans the entire drive, block by block, to find remnants of partition structures.

- Again, use p to preview files and confirm if a found partition is the one you are looking for.

### 7. Modify Partition Status
- After finding the correct partitions, use the Left/Right arrow keys to set their status.

- Use **Left/Right arrow keys** to change status:  
  - **P**: Primary  
  - ***:** Bootable  
  - **L**: Logical  
  - **D**: Deleted

    <br>
<br>
<img width="1100" height="634" alt="Screenshot 2025-09-02 152557" src="https://github.com/user-attachments/assets/caf363a1-9a5d-4e7e-9bc3-611a8c48440c" />


</p>
<br>
<br>

- Ensure that the partitions you want to recover are marked as Primary or Logical (and not deleted).

### 8. Write the Partition Table
- Once you are confident the partition structure is correct, select [Write] from the menu.

<br>
<br>
<img width="1100" height="633" alt="Screenshot 2025-09-02 152702" src="https://github.com/user-attachments/assets/ad31a133-40d3-4ff6-a596-66829018b850" />


<br>
<br>

- Confirm the operation by pressing y (for yes). This will write the new partition table to your disk.

<br>
<br>
<p align="center">
  <img width="1100" height="633" alt="Screenshot 2025-09-02 152702" src="https://github.com/user-attachments/assets/61098b03-0add-437c-a985-63b6add77b50" />


</p>
<br>
<br>


- WARNING: This is a permanent change. Double-check your selections before writing.

### 9. Recover Files
- If you just need to recover a few files without fixing the partition table, you can do so from the file list (after pressing p).

- Navigate to the folder containing your desired files.

- Use the colon : key to select the files you want to recover.

- Press the uppercase C key to copy the selected file(s).

- Navigate to a safe destination on a different storage device and press uppercase C again to paste.

### 10. Exit and Restart
- Once your task is complete, select [Quit] to exit the program.

- If you wrote a new partition table to the drive, it is recommended to restart your computer to allow the operating system to recognize the changes.

## Rubrics

| **Criteria & Marks Assigned**                                | **Mark Allotted** | **Mark Awarded** |
|--------------------------------------------------------------|-------------------|------------------|
|                                                                                                     |
| 1. GitHub Activity & Submission Regularity                   |         3         |                  |
|                                                                                                     |
| 2. Application of Forensic Tools & Practical Execution       |         3         |                  |
|                                                                                                     |
| 3. Documentation & Reporting                                 |         2         |                  |
|                                                                                                     |
| 4. Engagement, Problem-Solving & Team Collaboration          |         2         |                  |
|                                                                                                     |
|                  **Total**                                   |       **10**      |                  |
|                                                                                                     |

## Result : 
- Thus this experiment is successfully completed using TestDesk tool.
