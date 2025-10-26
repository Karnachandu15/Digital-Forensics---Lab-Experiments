# Experiment 9
# Use Process Explorer to Identify Suspicious Processes

---
## Aim
To demonstrate the use of Process Explorer in identifying, analyzing, and investigating suspicious processes running on a Windows system for digital forensics purposes.

---
## Description
Process Explorer is an advanced system monitoring tool that provides detailed information about which handles and DLLs processes have opened or loaded. This experiment focuses on using Process Explorer to identify potentially malicious processes, analyze their behavior, and determine their impact on system security.

---
## Tools Used
1. Process Explorer (Sysinternals Suite)
2. Windows Operating System
3. Test processes (both legitimate and suspicious)
4. VirusTotal integration (for malware verification)

---
## Prerequisites
1. Download and install Process Explorer from Microsoft Sysinternals
2. Administrative privileges on the Windows system
3. Internet connection (for VirusTotal integration)
4. Basic understanding of Windows processes

---
## Procedure

### 1. Installation and Setup
1. Download Process Explorer from Microsoft's website
2. Extract and run ProcessExplorer.exe
3. Configure Process Explorer settings:
   - Enable "Verify Image Signatures"
   - Configure VirusTotal integration
   
![Process Explorer setup](Output%20Screenshot/Exp9/Screenshot%20(123).png)
![Process Explorer setup](Output%20Screenshot/Exp9/Screenshot%20(124).png)

<!-- [Insert Screenshot: Place screenshot of Process Explorer initial setup] -->

### 2. Basic Process Analysis
1. Observe the two-pane display:
   - Upper pane: Process list
   - Lower pane: Handle or DLL view

![Process Explorer interface](Output%20Screenshot/Exp9/Screenshot%20(127).png)
<!-- [Insert Screenshot: Place screenshot showing Process Explorer main interface] -->

2. Understanding the color coding:
   - Purple: Packed processes
   - Pink: Services
   - Blue: New processes
   - Red: Terminated processes

![Process color coding](Output%20Screenshot/Exp9/Screenshot%20(126).1.png)
<!-- [Insert Screenshot: Place screenshot highlighting different process colors] -->

### 3. Identifying Suspicious Processes
1. Check for unusual process names or locations
2. Look for processes with:
   - No description
   - No company name
   - Suspicious file locations
   - High CPU or memory usage

### 4. Process Properties Analysis
1. Right-click suspicious process → Properties
2. Examine:
   - Image path
   - Command line
   - Parent process
   - Start time
   - User account
   
![Process properties](Output%20Screenshot/Exp9/Screenshot%20(130).png)
<!-- [Insert Screenshot: Place screenshot of process properties window] -->

### 5. VirusTotal Integration
1. Enable VirusTotal submission
2. Check suspicious files:
   - Right-click process
   - Select "Check VirusTotal"
   
![VirusTotal check](Output%20Screenshot/Exp9/Screenshot%20(137).png)
<!-- [Insert Screenshot: Place screenshot showing VirusTotal check results] -->

### 6. DLL and Handle Investigation
1. View loaded DLLs:
   - Select process
   - Lower pane: DLL view
   
![DLL investigation](Output%20Screenshot/Exp9/Screenshot%20(133).png)
<!-- [Insert Screenshot: Place screenshot of DLL investigation] -->

2. Analyze handles:
   - Switch to handle view
   - Look for suspicious file/registry handles
   
![Handle analysis](Output%20Screenshot/Exp9/Screenshot%20(138).png)
<!-- [Insert Screenshot: Place screenshot of handle analysis] -->

### 7. Tree View Analysis
1. View process relationships:
   - Enable tree view
   - Identify parent-child relationships
   
![Process tree view](Output%20Screenshot/Exp9/Screenshot%20(134).png)
<!-- [Insert Screenshot: Place screenshot of process tree view] -->

---
## Results
The experiment successfully demonstrated:

1. Process Identification:
   - Total processes analyzed: [X]
   - Suspicious processes identified: [X]
   - Confirmed malicious processes: [X]

2. System Analysis:
   - CPU usage patterns
   - Memory usage patterns
   - Network connection analysis
   - File handle investigation

3. Key Findings:
   - Types of suspicious activities detected
   - Common characteristics of malicious processes
   - System resource impact

---
## Conclusion
Process Explorer is an effective digital forensics tool for identifying and analyzing suspicious processes on Windows systems. 

Key benefits:
1. Real-time monitoring of all running processes
2. Quick identification of unsigned or suspicious executables
3. Easy verification of processes using VirusTotal
4. Detailed view of process relationships and loaded DLLs

The tool is recommended for initial system investigation and ongoing security monitoring of Windows environments.

---