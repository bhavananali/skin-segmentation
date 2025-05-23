README.txt
Assignment Title: Skin Segmentation Using Statistical Color Models
Roll Number: 24AI06013
Name: Nali Bhavana

Description
This assignment implements a skin segmentation algorithm based on the CVPR 1999 paper titled “Statistical Color Models with Application to Skin Detection.” The implementation uses manually masked training images to build a histogram model in HSV color space. It then performs backprojection on test images to estimate the likelihood of skin regions and applies morphological operations for refinement.

Files Included
- 24AI06013_CV_assgn2.ipynb – Main notebook containing the complete code.
- train1.jpg, train2.jpg, train3.jpg – Training images with skin regions manually masked.
- test1.jpg, test2.jpg – Test images used for skin detection.
- README.txt – This file.

How to Run
1. Ensure all the required image files are in the same directory as the notebook.
2. Open 24AI06013_CV_assgn2.ipynb in Google Colab or a Jupyter environment.
3. Run all cells in the notebook.
4. The script will display:
   - The original test image
   - The segmented result showing detected skin areas

Key Techniques
- HSV Color Space Conversion: BGR values are converted to HSV to better capture skin tone patterns.
- Histogram-Based Modeling: Histograms are built for Hue and Saturation channels based on training skin pixels.
- Backprojection: Used to calculate the skin likelihood for each pixel in the test image.
- Morphological Operations: Custom dilation and erosion using a circular kernel to improve mask quality.

Dependencies
- Python libraries:
  - opencv-python
  - numpy
  - matplotlib

Install using pip if not already available:

pip install opencv-python numpy matplotlib

Additional Notes
- BGR to HSV conversion is implemented manually to ensure control over the value ranges.
- Only basic OpenCV image read/write functions are used in accordance with the assignment instructions.
- The final result replaces non-skin regions with white pixels for clear visualization.
