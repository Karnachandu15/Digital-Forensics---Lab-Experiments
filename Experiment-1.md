# Experiment - 1
# Create a forensic image of a storage device's using FTK Imager.
---

## Aim
To create a forensically sound bit-stream image of a storage device (e.g., USB drive, hard disk) using FTK Imager, ensuring data integrity through hash verification.

---

## Description
Disk imaging is the process of creating an exact, sector-by-sector copy of a storage device. This copy, known as a forensic image, is crucial for digital forensics as it preserves the original evidence in an unaltered state. This allows an investigator to perform analysis on the image without any risk of modifying the original source evidence.

FTK Imager is a popular and widely used forensics tool developed by AccessData. It provides a user-friendly interface to create forensic images, verify their integrity using hash values (like MD5, SHA-1), and perform preliminary analysis.

This experiment involves connecting a source drive (via a write-blocker, if available), using FTK Imager to create a forensic image file, and generating a hash value to prove the image is an exact copy of the original.

---

## Tools & Equipment Used
- FTK Imager (Software)

- Source Drive: A USB flash drive (or hard disk) containing data.

- Destination Drive: An external hard drive with sufficient free space to store the image file.

---

## Procedure
**Launch FTK Imager**

  - Open the FTK Imager tool on your computer.
![Fig-1](<Output Screenshot/Exp1/Screenshot 2025-08-31 165800.png>)
  - Make sure you run it with administrative privileges so that the tool can access hardware devices properly.

**Select the Source Drive**

  - From the top menu, go to File → Create Disk Image.
![Fig-2](<Output Screenshot/Exp1/Screenshot (45).png>)
  - In the dialog box, choose the type of source. Usually, for a physical storage device, select Physical Drive.
![Fig-3](<Output Screenshot/Exp1/Screenshot (46).png>)
 - Click Next.

 - A list of available drives will appear. Select the storage device that you want to acquire and then click Finish.
![Fig-4](<Output Screenshot/Exp1/Screenshot (47).png>)

**Choose the Image Destination**

 - Once the source is added, FTK Imager will ask you to specify where the image should be saved.


 - Click Add, then select the desired Image Type. Common choices include:

    - E01 (EnCase Evidence File format) → widely used in forensics.

    - RAW (dd format) → bit-by-bit copy.
![Fig-5](<Output Screenshot/Exp1/Screenshot (48).png>)
   - Click Next.

**Enter Case Information Optional but Recommended**

    - A window will prompt for case details like:

        - Case Number

        - Evidence Number

        - Examiner Name

        - Notes (e.g., description of the device).

    - Fill in the details for proper documentation, then click Next.
![Fig-6](<Output Screenshot/Exp1/Screenshot (49).png>)
**Set Destination Path and File Name**

 - Browse and select the folder where you want to save the forensic image.

 - Provide a meaningful file name (e.g., USB_8GB_Evidence.E01).

 - Specify a segment size if required (default is fine in most cases).

 - Choose the compression level if using E01 format.

 - Click Finish.
![Fig-7](<Output Screenshot/Exp1/Screenshot (50).png>)
**Verify Image Options**

 - FTK Imager will now show a summary of the settings you selected.

 - Review them carefully to make sure the correct drive and destination are selected.

 - Click Start to begin the imaging process.
![Fig-8](<Output Screenshot/Exp1/Screenshot (55).png>)
**Imaging and Hash Verification**

 - FTK Imager will create the forensic image bit-by-bit from the source device.

 - Once completed, it will automatically calculate cryptographic hashes (MD5, SHA1) for both the source and the image.

 - Verify that the hashes match to confirm the integrity of the forensic image.

**Save the Log File**

 - After the process is finished, FTK Imager generates a log file containing all details (case info, hash values, acquisition time, etc.).

 - Save this log file along with the image, since it acts as proof of authenticity and integrity.
![Fig-9](<Output Screenshot/Exp1/Screenshot 2025-08-31 174812.png>)

---

## Result 
 - A forensic image of the selected storage device is successfully created using FTK Imager, along with hash verification and log documentation.