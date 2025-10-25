# Experiment 8: Use Steg-Expose to Detect Hidden Data in Images

## Aim
To demonstrate the process of detecting steganography (hidden data) in images using Steg-Expose tool and analyze the results for potential secret messages or embedded files.

## Description
Steg-Expose is a specialized steganalysis tool designed to detect steganography in image files. This experiment focuses on using Steg-Expose to analyze various image files and determine if they contain hidden data using statistical analysis methods. The tool combines multiple steganalysis techniques to identify potential steganographic content.

## Tools Used
1. Steg-Expose
2. Python 3.x
3. Test images (both clean and with hidden data)
4. Terminal/Command Prompt
5. Image manipulation tools (optional, for creating test cases)

## Prerequisites
1. Java Runtime Environment (JRE) installed
2. Download StegExpose from GitHub:
```bash
git clone https://github.com/b3dk7/StegExpose.git
```
3. Test images prepared (both with and without hidden data)

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

3. Test StegExpose:
```bash
java -jar StegExpose.jar -h
```
![StegExpose help menu](Output%20Screenshot/Exp8/stegexpose-help.png)
<!-- [Insert Screenshot: Place screenshot showing StegExpose help menu] -->

### 2. Preparing Test Images
1. Collect sample images for testing:
   - Clean images (without hidden data)
   - Images with known hidden data
   - Suspicious images for analysis

![test image collection](Output%20Screenshot/Exp8/test-images.png)
<!-- [Insert Screenshot: Place screenshot showing test image collection] -->

### 3. Basic Image Analysis
1. Analyze a single image:
```bash
stegexpose image1.jpg
```
![single image analysis](Output%20Screenshot/Exp8/single-image-analysis.png)
<!-- [Insert Screenshot: Place screenshot of single image analysis result] -->

2. Analyze multiple images in a directory:
```bash
stegexpose directory_path/
```
![batch analysis](Output%20Screenshot/Exp8/batch-analysis.png)
<!-- [Insert Screenshot: Place screenshot showing batch analysis results] -->

### 4. Advanced Detection Settings
1. Run analysis with custom threshold:
```bash
stegexpose -t 0.2 suspicious_image.png
```
![custom threshold analysis](Output%20Screenshot/Exp8/custom-threshold.png)
<!-- [Insert Screenshot: Place screenshot of analysis with custom threshold] -->

2. Generate detailed report:
```bash
stegexpose -csv report.csv image_folder/
```
![CSV report generation](Output%20Screenshot/Exp8/csv-report.png)
<!-- [Insert Screenshot: Place screenshot showing CSV report generation] -->

### 5. Statistical Analysis Methods
1. Primary Detection Techniques Used:
   - Sample Pair Analysis
   - RS Analysis
   - Chi-Square Attack
   - Primary Sets Analysis

![analysis methods](Output%20Screenshot/Exp8/analysis-methods.png)
<!-- [Insert Screenshot: Place screenshot showing different analysis methods] -->

### 6. Result Interpretation
1. Understanding the output scores:
   - 0.0 to 0.2: Likely clean
   - 0.2 to 0.4: Suspicious
   - Above 0.4: High probability of hidden content

![result interpretation](Output%20Screenshot/Exp8/result-interpretation.png)
<!-- [Insert Screenshot: Place screenshot showing result interpretation] -->

### 7. Validation Process
1. Compare results with known test cases
2. Document false positives and false negatives
![validation results](Output%20Screenshot/Exp8/validation-results.png)
<!-- [Insert Screenshot: Place screenshot of validation results] -->

## Results
The experiment successfully demonstrated:

1. Detection Capabilities:
   - Number of images analyzed: [X]
   - True positives: [X]
   - False positives: [X]
   - Detection accuracy: [X%]

2. Performance Metrics:
   - Average analysis time per image: [X] seconds
   - False positive rate: [X%]
   - Detection threshold effectiveness: [X%]

3. Tool Effectiveness:
   - Successfully identified [X] out of [Y] images with hidden data
   - Correctly classified [Z%] of clean images

## Analysis Findings

### 1. Detection Accuracy
- Different file formats analysis:
  - JPEG: [X%] accuracy
  - PNG: [X%] accuracy
  - BMP: [X%] accuracy

### 2. Limitations Observed
- File size limitations
- Format-specific detection rates
- Processing time considerations
- False positive scenarios

### 3. Best Practices Identified
1. Optimal threshold settings for different image types
2. Most effective analysis methods for various steganography techniques
3. Recommended workflow for bulk image analysis

## Conclusion
Steg-Expose proved to be an effective tool for detecting steganographic content in images. The experiment successfully demonstrated its capability to:
1. Identify potentially compromised images
2. Analyze large sets of images efficiently
3. Provide detailed statistical analysis of suspected steganographic content
4. Generate comprehensive reports for further investigation

The tool showed particular strength in [specific area] while having some limitations in [specific area]. For forensic investigations, it serves as a valuable initial screening tool for detecting hidden data in images.
