# Experiment - 2
# Recover deleted or damaged files from a storage device using Test Disk


# Experiment 2: Recover Deleted or Damaged Files from a Storage Device using TestDisk  

## Aim  
To recover deleted or damaged files from a storage device using **TestDisk**, a forensic recovery tool.  

---

## Description  
In digital forensics, recovering deleted or corrupted files is an essential step during investigations. When files are deleted, their entries are removed from the file system, but the actual data often remains on the storage media until overwritten. TestDisk is an open-source forensic tool designed to recover lost partitions, fix disk errors, and restore deleted files.  

In this experiment, we use TestDisk to identify and restore deleted or damaged files from a storage device, ensuring data integrity for forensic analysis.  

---

## Procedure  

1. **Launch TestDisk**  
   - Open the TestDisk tool (from command line or executable).  
   ![alt text](<Output Screenshot/Exp2/Screenshot (58).png>)
   - Run it with administrative privileges for full access.  

2. **Select Create/Append Log**  
   - On startup, choose **Create** to generate a log file for documentation.  
    ![alt text](<Output Screenshot/Exp2/Screenshot (59).png>)

3. **Choose the Storage Device**  
   - TestDisk lists all available storage devices.
    ![alt text](<Output Screenshot/Exp2/Screenshot (59).png>)
   - Use the arrow keys to select the target device.  


4. **Select Partition Table Type**  
   - TestDisk detects the partition table type (e.g., Intel/MBR, EFI GPT).
    ![alt text](<Output Screenshot/Exp2/Screenshot (60).png>)
   - Confirm the suggestion by pressing **Enter**. 


5. **Analyze the Disk**  
   - Select **Analyse** → Quick Search to find lost partitions.  
   ![alt text](<Output Screenshot/Exp2/Screenshot (61).png>)
   - Use **Deeper Search** if needed. 
    ![alt text](<Output Screenshot/Exp2/Screenshot (65).png>)
 

6. **Access Advanced Options**  
   - Go to **Advanced → File System Utilities**. 
    ![alt text](<Output Screenshot/Exp2/Screenshot (66).png>)
   - Select the partition where files were deleted. 
   - Press **Enter** to view files.  
 

7. **Recover Deleted Files**  
   - Deleted files are shown in red. 
    ![alt text](<Output Screenshot/Exp2/Screenshot (71).png>)
   - Highlight a file and press **C** (copy) to recover. 
    ![alt text](<Output Screenshot/Exp2/Screenshot (72).png>)
   - Choose a **different drive** as the destination to avoid overwriting data.  
 

8. **Verify Recovered Files**  
   - Open the destination folder and check if the files were restored correctly.  
   - Document the recovery in the log file.  

---

## Result  
Deleted or damaged files were successfully recovered from the storage device using TestDisk, and their integrity was preserved for forensic analysis.  
