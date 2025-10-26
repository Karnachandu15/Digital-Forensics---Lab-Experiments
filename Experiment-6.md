# Experiment - 6
# Use Sleuth Kit to Analyze Digital Evidence

---

## Aim
To understand and demonstrate the usage of Sleuth Kit in analyzing digital evidence for forensic investigation purposes.

---

## Description
The Sleuth Kit (TSK) is a powerful open-source digital forensics toolkit that enables investigators to analyze disk images and recover files. This experiment focuses on using various Sleuth Kit commands and tools to examine digital evidence, recover deleted files, and analyze file system artifacts.

---

## Tools Used
1. The Sleuth Kit (TSK)
2. Command Line Interface
3. Disk Image (for analysis)
4. AutopsyⓇ (GUI frontend for Sleuth Kit)

---

## Procedure

### 1. Installation and Setup
1. Download and install The Sleuth Kit from the official website
2. Verify the installation by running basic commands
3. Prepare a disk image for analysis

### 2. Basic File System Analysis
1. Use `mmls` to display the partition layout
    ```bash
    mmls Evidence.dd
    ```
    Note the Start Sector of the partition (e.g., 2048).

    ![mmls output](Output%20Screenshot/Exp6/Screenshot%202025-10-23%20222452.png)

<!-- [Insert Screenshot: Place the screenshot of mmls command output showing partition table] -->

2. Use `fsstat` to examine file system details
    ```bash
    fsstat -o 63 Evidence.raw
    ```
    ![fsstat output](Output%20Screenshot/Exp6/Screenshot%202025-10-23%20222446.png)

    <!-- [Insert Screenshot: Place the screenshot showing file system information] -->

### 3. File Recovery and Analysis
1. Use `fls` to list files and directories
    ```bash
    fls -o 63 Evidence.dd
    ```
    ![fls output 1](Output%20Screenshot/Exp6/Screenshot%202025-10-23%20224310.png)
    ![fls output 2](Output%20Screenshot/Exp6/Screenshot%202025-10-23%20222608.png)
    <!-- [Insert Screenshot: Place the screenshot showing file listing] -->

2. Use `icat` to extract files using their inode numbers and to recover
    ```bash
    icat evidence_disk.dd inode_number > recovered_file
    ```
    ![icat output](Output%20Screenshot/Exp6/Screenshot%202025-10-23%20222954.png)

    <!-- [Insert Screenshot: Place the screenshot of file recovery process] -->



<!-- ### 4. Timeline Analysis
1. Create a timeline of file activity
```bash
fls -m "/" evidence_disk.dd > body.txt
mactime -b body.txt > timeline.txt
```
[Insert Screenshot: Place the screenshot showing timeline analysis] -->

<!-- ### 5. Deleted File Recovery
1. Use `ils` to list deleted inodes
```bash
ils evidence_disk.dd
``` -->
<!-- [Insert Screenshot: Place the screenshot showing deleted inodes] -->

### 4. Analyze Metadata
    1. use this command to displays timestamps, size, and allocation info for that file.

    ```bash
    istat -o 63 Evidence 6342-128-4
    ```
![istat output](Output%20Screenshot/Exp6/Screenshot%202025-10-23%20222950.png)

---

## Results
The experiment successfully demonstrated:

1. Basic file system analysis capabilities of Sleuth Kit
2. File system structure examination and interpretation
3. Recovery of both active and deleted files
4. Timeline analysis of file system activities
5. Understanding of digital forensics investigation workflow using Sleuth Kit

Key findings included:
- Successfully identified partition structure
- Retrieved file system metadata
- Recovered deleted files
- Created comprehensive timeline of file system activities
- Demonstrated proper digital forensics investigation procedures

---

## Conclusion
The Sleuth Kit proves to be an essential tool in digital forensics investigations, providing detailed insights into file systems and enabling investigators to recover and analyze digital evidence effectively. Through this experiment, we gained practical experience in using various Sleuth Kit commands and understanding their application in real-world forensic scenarios.

---
