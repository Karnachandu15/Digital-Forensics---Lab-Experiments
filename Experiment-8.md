# Experiment 8 
# Use Steg-Expose to Detect Hidden Data in Images

---
## Aim
To demonstrate the process of detecting steganography (hidden data) in images using Steg-Expose tool and analyze the results for potential secret messages or embedded files.

---
## Description
Steg-Expose is a specialized steganalysis tool designed to detect steganography in image files. This experiment focuses on using Steg-Expose to analyze various image files and determine if they contain hidden data using statistical analysis methods. The tool combines multiple steganalysis techniques to identify potential steganographic content.

---
## Tools Used
1. Steg-Expose
2. Python 3.x
3. Test images (both clean and with hidden data)
4. Terminal/Command Prompt
5. Image manipulation tools (optional, for creating test cases)

---
## Prerequisites
1. Java Runtime Environment (JRE) installed
2. Download StegExpose from GitHub:
```bash
git clone https://github.com/b3dk7/StegExpose.git
```
3. Test images prepared (both with and without hidden data)

---
## Procedure

### 1. Installation and Setup
1. Navigate to StegExpose directory:
```bash
cd StegExpose
```

2. Verify Java installation:
```bash
java -version
```

### 2. Preparing Test Images
1. Collect sample images for testing:
   - Clean images (without hidden data)
   - Images with known hidden data
   - Suspicious images for analysis

![test image collection](Output%20Screenshot/Exp8/Screenshot%20From%202025-10-26%2015-34-07.png)
<!-- [Insert Screenshot: Place screenshot showing test image collection] -->

### 3. Basic Image Analysis

1. Analyze images in a directory:
```bash
java -jar StegExpose.jar /home/kali/Downloads/testingsteg -a -r result1.csv
```
this will make the result to save in the .CSV file
![batch analysis](Output%20Screenshot/Exp8/Screenshot%20From%202025-10-26%2015-00-32.png)
<!-- [Insert Screenshot: Place screenshot showing batch analysis results] -->

### 4. Analyze the Output
1. After running the tool, it will analyze the image and provide a score.

2. Output Explanation:
   - StegExpose calculates a "suspect" score (between 0 and 1). The higher the score, the more likely that hidden data is present.
   - Threshold values (suggested by the tool):
   - Less than 0.2: Image is clean (no hidden data).
   - 0.2 - 0.3: Possibly some hidden data.
   - Above 0.3: Likely that steganography is present.

![report image](Output%20Screenshot/Exp8/Screenshot%20From%202025-10-26%2015-55-16.png)
<!-- [Insert Screenshot: Place screenshot showing CSV report generation] -->


### 5. Result Interpretation
1. Understanding the output scores:
   - 0.0 to 0.2: Likely clean
   - 0.2 to 0.4: Suspicious
   - Above 0.4: High probability of hidden content

![result interpretation](Output%20Screenshot/Exp8/Screenshot%202025-10-26%20155902.png)
<!-- [Insert Screenshot: Place screenshot showing result interpretation] -->

---

## Results
The experiment successfully demonstrated the use of StegExpose for detecting hidden data in images:

1. **Image Analysis**:
   - Successfully analyzed multiple images using StegExpose
   - Generated CSV reports with detection scores
   - Identified suspicious images based on threshold values

2. **Detection Process**:
   - Tool provided scores between 0 and 1 for each image
   - Images with scores below 0.2 were classified as clean
   - Images with scores above 0.3 indicated likely presence of hidden data

3. **Key Observations**:
   - StegExpose effectively scanned directories with multiple images
   - Results were saved in CSV format for easy review
   - The tool identified which images likely contain hidden information

---
## Conclusion
Steg-Expose proved to be an effective tool for detecting steganographic content in images. The experiment successfully demonstrated its capability to:
1. Identify potentially compromised images
2. Analyze large sets of images efficiently
3. Provide detailed statistical analysis of suspected steganographic content
4. Generate comprehensive reports for further investigation

The tool showed particular strength in [specific area] while having some limitations in [specific area]. For forensic investigations, it serves as a valuable initial screening tool for detecting hidden data in images.

---