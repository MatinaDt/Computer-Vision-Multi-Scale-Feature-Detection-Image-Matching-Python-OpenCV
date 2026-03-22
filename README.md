# Multi-Scale Feature Detection & Image Matching

## Overview
This project implements classical **Computer Vision algorithms** for detecting and describing key image features, with applications in image matching and classification.

The focus is on building a full pipeline from low-level image processing to high-level feature-based recognition, including robustness to **noise, scale, and geometric transformations**.

---

## Objectives
- Detect edges, corners, and blobs in images
- Implement multi-scale feature detection
- Extract robust local descriptors
- Perform feature matching under transformations
- Classify images using visual features

---

## Methods

### 1. Edge Detection
- Gaussian smoothing
- Laplacian of Gaussian (LoG)
- Zero-crossing detection
- Gradient-based thresholding

✔ Evaluated using precision, recall, and detection quality metrics

---

### 2. Corner Detection (Harris)
- Structure tensor computation
- Eigenvalue-based corner response
- Non-maximum suppression
- Threshold filtering

---

### 3. Blob Detection
- Hessian matrix determinant
- Detection of homogeneous regions (blobs)
- Multi-scale extension (scale-space analysis)

---

### 4. Multi-Scale Feature Detection
- Scale pyramid using Gaussian kernels
- Automatic scale selection using Laplacian response
- Detection across different spatial resolutions

---

### 5. Feature Descriptors
- **SURF** (Speeded-Up Robust Features)
- **HOG** (Histogram of Oriented Gradients)

Used to encode local image structure around detected keypoints.

---

### 6. Image Matching
- Matching descriptors across transformed images
- Robust to:
  - Rotation
  - Scaling
- Evaluation of matching accuracy

---

### 7. Image Classification
- Bag of Visual Words (BoVW)
- Feature clustering (k-means)
- Classification using SVM

---

## Results

The system was evaluated on:
- Noisy images (PSNR variations)
- Real-world images
- Transformed datasets (scale + rotation)

### Key Findings:
- Larger Gaussian scale improves noise robustness but reduces detail
- Multi-scale detection is essential for real-world performance
- SURF descriptors outperform HOG in matching tasks
- Feature-based pipelines provide strong invariance to transformations

---

## Tech Stack
- Python
- OpenCV
- NumPy
- SciPy
- Matplotlib

---
