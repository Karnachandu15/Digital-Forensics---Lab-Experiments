# Experiment - 5
# Use Autopsy to Create a Case and Import Evidence
---

## Aim
To learn how to create a new case in Autopsy Digital Forensics Tool and import digital evidence for analysis.

---

## Tools
- Autopsy 4.21.0 or later
- Sample digital evidence file (disk image, USB image, or any other supported format)

---

## Description
Autopsy is a popular open-source digital forensics platform used by law enforcement, military, and corporate examiners to investigate what happened on a computer. It has a graphical interface that allows forensic investigators to analyze disk images, perform timeline analysis, and recover deleted files.

---
## Procedure

1. **Launch Autopsy**
   - Open Autopsy digital forensics tool
   - Wait for the application to initialize
   
   ![Autopsy welcome screen](Output%20Screenshot/Exp5/Screenshot%202025-10-23%20193917.png)

2. **Create New Case**
   - Click on "Create New Case" option
   - Enter case name, base directory for case storage
   - Fill in optional case details (examiner name, case number, etc.)
   
   ![New case creation](Output%20Screenshot/Exp5/Screenshot%202025-10-23%20193953.png)

3. **Configure Case Database**
   - Select the database type (Single-user or Multi-user)
   - Choose the database location
   - Click "Next" to proceed

4. **Add Data Source**
   - Click "Add Data Source" in the main window
   - Select the type of data source (disk image, local drive, logical files)
   - Browse and select the evidence file
   
   ![Add data source](Output%20Screenshot/Exp5/Screenshot%202025-10-23%20194311.png)

5. **Configure Ingest Modules**
   - Select relevant ingest modules for analysis
     - Recent Activity
     - Hash Lookup
     - File Type Identification
     - Keyword Search
     - EXIF Parser
     - etc.
   - Configure settings for selected modules
   
   ![Ingest modules](Output%20Screenshot/Exp5/Screenshot%202025-10-23%20194505.png)

6. **Start Analysis**
   - Review selected options
   - Click "Finish" to begin processing
   - Monitor ingest progress
   
   ![Analysis progress 1](Output%20Screenshot/Exp5/Screenshot%202025-10-23%20194512.png)
   ![Analysis progress 2](Output%20Screenshot/Exp5/Screenshot%202025-10-23%20194545.png)

---

## Result
After completing this experiment, you should be able to:
1. Successfully create a new case in Autopsy
2. Import digital evidence into the case
3. Configure appropriate ingest modules for analysis
4. Begin the forensic analysis process

---
The imported evidence will be ready for detailed forensic analysis using Autopsy's various tools and features. The case structure is now set up to maintain proper chain of custody and documentation of the investigation process.

![Final case view](Output%20Screenshot/Exp5/Screenshot%202025-10-23%20210153.png)

Note: Remember to document all steps and maintain proper chain of custody throughout the process. Each action taken in Autopsy is logged and can be reviewed later as part of the investigation documentation.

---