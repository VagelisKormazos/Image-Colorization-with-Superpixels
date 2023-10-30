# Image Colorization with Superpixels and Local Regression

This repository contains a Python script for image colorization using superpixels and local regression. The implemented workflow includes the following steps:

## Workflow Overview

1. **Image Representation in the Lab Color Space:**
   - Load images from a specified folder.
   - Convert images from the RGB color space to the Lab color space.

2. **SURF Feature Extraction:**
   - Compute SURF (Speeded-Up Robust Features) descriptors for each image.

3. **Superpixel Segmentation with SLIC:**
   - Apply the SLIC (Simple Linear Iterative Clustering) algorithm to segment images into superpixels.

4. **Color Information Extraction from Superpixels:**
   - For each superpixel, compute the mean Lab color.

5. **Data Splitting for Training and Testing:**
   - Split the data into training and testing sets.

6. **Local Regression with LinearSVR:**
   - Train a Linear Support Vector Regression (LinearSVR) model for predicting color values.

7. **Prediction and Visualization:**
   - Predict color values on the test set.
   - Visualize the original image with superpixel boundaries and the predicted coloring with superpixel boundaries.

8. **Optional Model Saving:**
   - Optionally, save the trained LinearSVR model.

## Dependencies

- OpenCV
- scikit-image
- scikit-learn
- joblib
- matplotlib

Install the required dependencies using:

```bash
pip install opencv-python scikit-image scikit-learn joblib matplotlib
