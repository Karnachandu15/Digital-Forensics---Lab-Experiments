# Experiment 9: Use Process Explorer to Identify Suspicious Processes

## Aim
To demonstrate the use of Process Explorer in identifying, analyzing, and investigating suspicious processes running on a Windows system for digital forensics purposes.

## Description
Process Explorer is an advanced system monitoring tool that provides detailed information about which handles and DLLs processes have opened or loaded. This experiment focuses on using Process Explorer to identify potentially malicious processes, analyze their behavior, and determine their impact on system security.

## Tools Used
1. Process Explorer (Sysinternals Suite)
2. Windows Operating System
3. Test processes (both legitimate and suspicious)
4. VirusTotal integration (for malware verification)

## Prerequisites
1. Download and install Process Explorer from Microsoft Sysinternals
2. Administrative privileges on the Windows system
3. Internet connection (for VirusTotal integration)
4. Basic understanding of Windows processes

## Procedure

### 1. Installation and Setup
1. Download Process Explorer from Microsoft's website
2. Extract and run ProcessExplorer.exe
3. Configure Process Explorer settings:
   - Enable "Verify Image Signatures"
   - Configure VirusTotal integration
   
[Insert Screenshot: Place screenshot of Process Explorer initial setup]

### 2. Basic Process Analysis
1. Observe the two-pane display:
   - Upper pane: Process list
   - Lower pane: Handle or DLL view

[Insert Screenshot: Place screenshot showing Process Explorer main interface]

2. Understanding the color coding:
   - Purple: Packed processes
   - Pink: Services
   - Blue: New processes
   - Red: Terminated processes
   
[Insert Screenshot: Place screenshot highlighting different process colors]

### 3. Identifying Suspicious Processes
1. Check for unusual process names or locations
2. Look for processes with:
   - No description
   - No company name
   - Suspicious file locations
   - High CPU or memory usage
   
[Insert Screenshot: Place screenshot showing suspicious process identification]

### 4. Process Properties Analysis
1. Right-click suspicious process → Properties
2. Examine:
   - Image path
   - Command line
   - Parent process
   - Start time
   - User account
   
[Insert Screenshot: Place screenshot of process properties window]

### 5. VirusTotal Integration
1. Enable VirusTotal submission
2. Check suspicious files:
   - Right-click process
   - Select "Check VirusTotal"
   
[Insert Screenshot: Place screenshot showing VirusTotal check results]

### 6. DLL and Handle Investigation
1. View loaded DLLs:
   - Select process
   - Lower pane: DLL view
   
[Insert Screenshot: Place screenshot of DLL investigation]

2. Analyze handles:
   - Switch to handle view
   - Look for suspicious file/registry handles
   
[Insert Screenshot: Place screenshot of handle analysis]

### 7. Tree View Analysis
1. View process relationships:
   - Enable tree view
   - Identify parent-child relationships
   
[Insert Screenshot: Place screenshot of process tree view]

### 8. Advanced Analysis
1. Stack traces
2. Thread analysis
3. Network connections
[Insert Screenshot: Place screenshot of advanced analysis features]

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

## Analysis Summary

### 1. Process Characteristics
- Identified suspicious patterns:
  - Unusual file locations
  - Suspicious DLL loading
  - Abnormal parent-child relationships
  - Unexpected network connections

### 2. System Impact
- Resource utilization
- System stability
- Network activity
- File system changes

### 3. Investigation Techniques
1. Effective methods for identifying suspicious processes
2. Verification procedures using VirusTotal
3. Documentation of findings
4. Response procedures

## Conclusion
Process Explorer proved to be a powerful tool for digital forensics investigation by:

1. Providing detailed process information
2. Enabling real-time monitoring of system activities
3. Facilitating malware identification
4. Supporting in-depth analysis of suspicious processes

The tool demonstrated particular effectiveness in:
- Identifying hidden processes
- Analyzing process relationships
- Detecting unusual system behavior
- Supporting malware investigation

Best Practices Identified:
1. Regular system monitoring
2. Baseline process knowledge
3. Systematic investigation approach
4. Proper documentation of findings

[Note: Please add actual screenshots of your experiment execution in the designated places marked with "Insert Screenshot" tags. Also, replace all placeholder values in square brackets with actual experimental data.]