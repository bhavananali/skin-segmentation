## Overview

This project implements a skin segmentation algorithm based on the CVPR 1999 paper titled  
**"Statistical Color Models with Application to Skin Detection."**

The model uses manually masked training images to build a skin color histogram in HSV color space.  
It performs backprojection on test images to estimate the likelihood of skin regions, followed by morphological operations for refinement.

## Files Included

- `24AI06013_CV_assgn2.ipynb` – Main notebook containing the complete code.
- `train1.jpg`, `train2.jpg`, `train3.jpg` – Training images with manually masked skin regions.
- `test1.jpg`, `test2.jpg` – Test images used for skin detection.
- `README.md` – This file.

## How to Run

1. Ensure all image files are in the same directory as the notebook.
2. Open `24AI06013_CV_assgn2.ipynb` in Google Colab or a Jupyter environment.
3. Run all cells in the notebook.
4. The following will be displayed:
   - Original test image
   - Segmented result showing detected skin areas

## Key Techniques

- **HSV Color Space Conversion**: Converts BGR images to HSV to better capture skin tone characteristics.
- **Histogram-Based Modeling**: Builds 2D histograms for the Hue and Saturation channels using skin pixels from training images.
- **Backprojection**: Estimates the skin likelihood for each pixel in the test image based on the histogram model.
- **Morphological Operations**: Applies custom dilation and erosion using a circular kernel to clean up the skin mask.

## Dependencies

Make sure the following Python libraries are installed:

- `opencv-python`
- `numpy`
- `matplotlib`

Install via pip if needed:

```bash
pip install opencv-python numpy matplotlib
