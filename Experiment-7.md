# Experiment 7: Android Device Forensic Acquisition using ADB Logical Backup

## Aim
To perform logical acquisition of data from an Android device using Android Debug Bridge (ADB) backup functionality.

## Description
This experiment demonstrates the forensic acquisition of data from an Android device using ADB's built-in backup functionality. The process includes creating a logical backup, verifying its integrity through hashing, and analyzing the extracted contents while maintaining forensic principles.

## Tools Used
1. Android Debug Bridge (ADB)
2. Android Device
3. USB Cable
4. Android Backup Extractor (abe.jar)
      .Download Android Backup Extractor from GitHub:
   ```bash
   git clone https://github.com/nelenkov/android-backup-extractor/releases/tag/latest
   ```
5. SHA256 hashing tool

## Prerequisites
1. Android device with:
   - USB debugging enabled
   - At least 50% battery life
   - Device unlocked and screen active
2. Computer with:
   - ADB installed and configured
   - Java Runtime Environment (JRE)
   - Required USB drivers installed

## Procedure

### 1. Device Connection and Verification
1. Connect Android device via USB
2. Verify connection using ADB:
```powershell
   adb devices
```
![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-23 231526.png>)
<!-- [Insert Screenshot: ADB devices list output] -->

3. Check device details:
```powershell
   adb shell getprop ro.product.model
   adb shell getprop ro.build.version.release
```
![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-23 233804.png>)
<!-- [Insert Screenshot: Device properties output] -->

### 2. Creating Full ADB Logical Backup
1. Create full backup including shared storage:
```powershell
   adb backup -f device_backup.ab -all -system -shared -apk
```
![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-23 234009.png>)
<!-- [Insert Screenshot: Backup creation dialog on device] -->

2. Monitor backup progress:
```powershell
   dir device_backup.ab
```
![alt text](<Output Screenshot\Exp6\Screenshot 2025-10-23 222950.png>)
<!-- [Insert Screenshot: File size and creation time] -->

### 3. Backup Integrity Verification
1. Generate SHA256 hash of backup file:
```powershell
   certutil -hashfile device_backup.ab SHA256
```
![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-23 234443.png>)
<!-- [Insert Screenshot: Hash output] -->

### 4. Creating External Storage Only Backup
1. Verify connection using ADB:
```powershell
   adb devices
```
![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-24 230100.1.png>)
<!-- [Insert Screenshot: Shared storage backup dialog] -->

2. Find the external storage path:
```powershell
   adb shell ls /storage
```
   You’ll see something like:
emulated  self  XXXX-XXXX
The one with numbers (e.g. XXXX-XXXX) is your SD card.

![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-24 230100.1.2.png>)

3. Create a backup folder on the host computer, for example:
```poweshell
   mkdir D:\android_backup
```

4. Back up only the SD card folder:
Replace XXXX-XXXX with your card ID:
```powershell
   adb pull /storage/XXXX-XXXX D:\phone_backup\
```
🔹 This copies only SD card contents to your laptop (folder D:\android_backup\).
🔹 It won’t touch internal storage or system data.

5. Verify backup creation:

![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-24 225851.png>)
<!-- [Insert Screenshot: Shared storage backup file details] -->

6. Compare sizes of full backup vs shared storage backup:
![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-24 225926.png>)
<!-- [Insert Screenshot: Size comparison of backup files] -->


### 5. Converting Backup to TAR Format
1. Download Android Backup Extractor (abe.jar)
2. Convert .ab file to .tar:
```powershell
   tar -cvf sd_backup.tar "C:\Users\K CHANDRA SEKHAR\backup"
```
![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-24 233410.png>)
![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-24 233430.png>)
<!-- [Insert Screenshot: Conversion process output] -->

### 6. Extracting Backup Contents
1. Extract TAR archive:
```powershell
   tar -xvf sd_backup.tar -C D:\extracted_backup\
```
![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-24 234127.png>)
<!-- [Insert Screenshot: Extraction process] -->

2. List extracted contents:
```powershell
   dir extracted_backup /s
```
![alt text](<Output Screenshot\Exp7\Screenshot 2025-10-24 234421.png>)
<!-- [Insert Screenshot: Directory listing] -->

### 7. Data Analysis

1. Common locations to examine:
   - apps/com.android.providers.contacts/d_*/databases/contacts2.db
   - apps/com.android.providers.telephony/d_*/databases/mmssms.db
   - apps/com.android.providers.media/d_*/databases/external.db

2. Analyze database contents using SQLite Browser

## Results
Document the following findings:
1. Backup File Details:
   - Size: [Size in MB]
   - Creation Time: [Timestamp]
   - SHA256 Hash: [Hash value]

2. Extracted Content Statistics:
   - Number of applications: [Count]
   - Total files extracted: [Count]
   - Key databases found: [List]

## Analysis Findings
1. Data Accessibility:
   - Successfully extracted user data
   - Located and analyzed key databases
   - Retrieved media files from shared storage

2. Process Validation:
   - Maintained forensic integrity through hashing
   - Documented all steps and findings
   - Preserved original backup file

## Conclusion
The experiment successfully demonstrated the process of performing logical acquisition from an Android device using ADB backup. This method proves effective for basic forensic acquisition while maintaining evidence integrity through proper documentation and hash verification.
