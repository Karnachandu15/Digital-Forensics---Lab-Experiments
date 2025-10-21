# Experiment 7: Use AFLogical OSE to Extract Data from an Android Device

## Aim
To demonstrate the process of extracting digital evidence and user data from an Android device using AFLogical OSE (Open Source Edition) forensics tool.

## Description
AFLogical OSE is an open-source mobile forensics tool designed specifically for Android devices. This experiment focuses on using AFLogical OSE to extract various types of data including SMS messages, call logs, contacts, and other user data from an Android device in a forensically sound manner.

## Tools Used
1. AFLogical OSE Application
2. Android Device (with USB debugging enabled)
3. USB Cable
4. Computer with ADB (Android Debug Bridge) installed
5. Data viewing software (for analyzing extracted data)

## Prerequisites
1. Android device with:
   - USB debugging enabled
   - At least 50% battery life
   - Sufficient storage space
2. Computer with:
   - ADB installed and configured
   - Java Runtime Environment (JRE)
   - USB drivers for the target Android device

## Procedure

### 1. Preparation Phase
1. Enable Developer Options on Android device
   - Go to Settings → About Phone
   - Tap "Build Number" seven times
   - Enable USB debugging in Developer Options
   
[Insert Screenshot: Place screenshot showing enabled USB debugging]

2. Install and configure ADB on the computer
```powershell
# Verify ADB installation
adb version
```
[Insert Screenshot: Place screenshot of ADB version verification]

### 2. Device Connection
1. Connect the Android device to the computer via USB
2. Accept USB debugging prompt on the device
3. Verify device connection using:
```powershell
adb devices
```
[Insert Screenshot: Place screenshot showing connected device in ADB]

### 3. AFLogical OSE Installation and Setup
1. Download AFLogical OSE APK
2. Install AFLogical OSE on the target device:
```powershell
adb install AFLogical-OSE.apk
```
[Insert Screenshot: Place screenshot of successful installation]

### 4. Data Extraction Process
1. Launch AFLogical OSE on the Android device
2. Select data types to extract:
   - SMS Messages
   - Call Logs
   - Contacts
   - Browser History
   - Calendar Events
   
[Insert Screenshot: Place screenshot of data selection screen]

3. Initialize extraction process
[Insert Screenshot: Place screenshot showing extraction progress]

4. Monitor extraction progress
[Insert Screenshot: Place screenshot of extraction completion]

### 5. Data Collection and Transfer
1. Locate extracted data on the device
```powershell
adb pull /sdcard/AFLogical/
```
[Insert Screenshot: Place screenshot showing data transfer to computer]

### 6. Data Analysis
1. Navigate to extracted data folder
2. Review extracted CSV files:
   - SMS.csv
   - Calls.csv
   - Contacts.csv
   - Browser.csv
   - Calendar.csv
   
[Insert Screenshot: Place screenshot showing extracted files structure]

### 7. Data Verification
1. Open extracted files using spreadsheet software
2. Verify data integrity and completeness
[Insert Screenshot: Place screenshot of data verification process]

## Results
The experiment successfully demonstrated:

1. Proper setup and configuration of AFLogical OSE
2. Successful extraction of various data types:
   - SMS Messages: [Number of messages extracted]
   - Call Logs: [Number of calls recorded]
   - Contacts: [Number of contacts retrieved]
   - Browser History: [Number of entries found]
   - Calendar Events: [Number of events extracted]

Key Achievements:
- Established secure connection with target device
- Completed data extraction without altering device contents
- Successfully transferred and verified extracted data
- Maintained forensic integrity throughout the process

## Analysis Findings
1. Data Completeness:
   - Successfully extracted all targeted data types
   - Preserved metadata including timestamps
   - Maintained data structure integrity

2. Tool Effectiveness:
   - AFLogical OSE performed reliably
   - Extraction process was non-invasive
   - Data output format was easily analyzable

## Conclusion
AFLogical OSE proved to be an effective tool for basic Android device forensics. The experiment successfully demonstrated the complete process of extracting digital evidence from an Android device while maintaining forensic integrity. The extracted data provides valuable insights for digital forensic investigations and can be further analyzed using specialized forensic tools.

[Note: Please add actual screenshots of your experiment execution in the designated places marked with "Insert Screenshot" tags]