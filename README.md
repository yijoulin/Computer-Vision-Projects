# Computer Vision Algorithms Portfolio

This repository presents a collection of classical computer vision algorithms implemented from scratch, covering image processing, feature extraction, video analysis, and object detection.

The goal of this project is to build a deep understanding of core computer vision techniques and their real-world behavior beyond high-level library usage.

---

## Overview

This project includes:

- Image transformation (rotation, skewing)
- Convolution-based filtering (smoothing, edge detection)
- Video scene change detection
- Texture feature extraction and classification
- Object segmentation and counting in video

All methods are implemented with minimal reliance on high-level APIs to emphasize algorithmic understanding.

---


---

## Notebooks

### 1. Image Transformation  
**File:** `image_transformation.ipynb`

**Problem**  
Apply geometric transformations without losing pixel information or introducing artifacts.

**Approach**
- Rotation matrix transformation  
- Inverse mapping to avoid pixel gaps  
- Center-based coordinate transformation  
- Skew transformation using affine matrices  

**Key Takeaways**
- Inverse mapping prevents missing pixels  
- Transformation order affects final results  
- Proper coordinate handling is critical  

---

### 2. Convolution Filters  
**File:** `convolution_filters.ipynb`

**Problem**  
Enhance images and extract useful features using filtering techniques.

**Approach**
- Average filtering (smoothing)  
- Gaussian blur  
- Laplacian filter (edge detection)  
- Zero padding to preserve image size  
- Sequential filtering (A→A, A→B, B→A)

**Key Takeaways**
- Gaussian filters reduce noise but blur details  
- Laplacian filters highlight edges  
- Filter order significantly impacts output  

---

### 3. Video Sequence Analysis (Histogram Intersection)  
**File:** `histogram_intersection.ipynb`

**Problem**  
Detect scene changes in video sequences.

**Approach**
- RGB histogram extraction  
- Histogram intersection  
- Normalized similarity (range [0,1])  
- Frame-by-frame comparison  

**Key Takeaways**
- Effective for detecting global scene changes  
- Sensitive to brightness and color shifts  
- Limitation: fails when spatial information is lost (same histogram, different images)

---

### 4. Texture Descriptors & Classification  
**File:** `texture_classification.ipynb`

**Problem**  
Represent and classify textures in images.

**Approach**
- Local Binary Pattern (LBP)  
- Window-based feature extraction  
- Histogram descriptors  
- Global feature aggregation  
- Euclidean distance similarity  

**Key Takeaways**
- Aggregated descriptors improve classification  
- Texture features enable class separation (e.g., face vs car)  
- Window size has limited impact on performance  

---

### 5. Object Segmentation & Counting  
**File:** `object_segmentation.ipynb`

**Problem**  
Detect and count moving objects in video.

**Approach**
- Frame differencing  
- Thresholding  
- Background modeling (temporal averaging)  
- Median filtering (denoising)  
- Morphological operations (dilation)  
- Connected components (DFS)

**Key Takeaways**
- Background modeling improves detection of distant objects  
- Noise vs object separation is a key challenge  
- Pipeline design strongly affects counting accuracy  

---

## Key Learning Outcomes

- Built core computer vision algorithms from first principles  
- Understood trade-offs between noise reduction, feature preservation, and accuracy  
- Developed full pipelines for both image and video processing  
- Gained practical insight into classical (pre-deep learning) computer vision methods  

---

## Tech Stack

- Python  
- NumPy  
- OpenCV (limited use)  
- Matplotlib  

---

## Applications

These methods are foundational in real-world systems such as:

- Autonomous driving (edge detection, segmentation)  
- Video surveillance (object detection & counting)  
- Content analysis (scene change detection)  
- Image enhancement pipelines  

---

## Full Report

For detailed explanations and results:

📄 `report/report.pdf`

---

## Notes

This project focuses on algorithmic understanding and implementation rather than production optimization.
