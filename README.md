# Corner Detection and Image Stitching

## Overview
This project consists of two main components:
1. Paper corner detection in video
2. Panoramic image stitching
---
   
![Screenshot from 2025-01-12 02-52-41](https://github.com/user-attachments/assets/ac6f9e78-adc2-469d-82f6-fd1c0d16f5db)

---
![Screenshot from 2025-01-12 02-51-20](https://github.com/user-attachments/assets/c2e4398d-83b7-427b-bccb-7848aa6c0904)

![Screenshot from 2025-01-12 02-51-31](https://github.com/user-attachments/assets/bedfc760-d38d-4e4f-b18e-2e24a94aa436)

![Screenshot from 2025-01-12 02-51-42](https://github.com/user-attachments/assets/53358bed-a09a-4256-90ce-c73aa6b99e22)

## Part 1: Paper Corner Detection

### Objectives
1. Implement a video processing pipeline for paper corner detection
2. Remove blurry frames using Variance of Laplacian
3. Detect and highlight paper corners
4. Create output video with overlaid results

### Implementation Pipeline
1. **Frame Processing**
   - Extract frames using OpenCV
   - Detect and remove blurry frames (threshold < 150)

2. **Edge Detection**
   - Background segmentation
   - Edge pixel detection
   - Hough Transform implementation

3. **Corner Detection**
   - Line intersection computation
   - Harris corner verification
   - Corner filtering and selection

4. **Visualization**
   - Blue boundary lines overlay
   - Red corner points marking
   - Output video generation

## Part 2: Panoramic Image Stitching

### Objectives
Create panoramic images from multiple overlapping photographs

### Implementation Pipeline
1. **Feature Extraction**
   - Custom feature detector implementation
   - Feature matching between consecutive images

2. **Image Alignment**
   - RANSAC-based feature matching
   - Homography computation
   - Image warping

3. **Image Stitching**
   - Combine frames using computed homographies
   - Handle overlapping regions
   - Generate final panorama

### Technical Constraints
- No `cv2.createStitcher`
- No direct stitching functions
- No `imutils` package
- Custom implementation of core algorithms

## Usage
1. Run notebooks in Google Colab
2. Upload input images/video
3. Execute cells sequentially
4. Check output visualizations

## Technical Requirements
- Python 3.x
- OpenCV
- NumPy
- Matplotlib
- Google Colab
