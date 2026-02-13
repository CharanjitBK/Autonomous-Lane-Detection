# Autonomous Lane Detection

This project implements a classical computer vision–based pipeline for detecting road lane markings from vehicle camera images. It focuses on efficiency, interpretability, and performance without using deep learning models.

## Motivation

Reliable lane detection is essential for autonomous driving and Advanced Driver Assistance Systems (ADAS).  
This project provides a lightweight and explainable solution using classical image processing techniques.

## Methodology

The lane detection pipeline consists of the following stages:

1. **Color Filtering**
   - Isolates white and yellow lane markings

2. **Grayscale Conversion & Gaussian Blur**
   - Reduces noise
   - Simplifies image structure

3. **Canny Edge Detection**
   - Highlights lane boundaries

4. **Region of Interest (ROI) Masking**
   - Focuses on the road area
   - Removes irrelevant regions (sky, vehicles, etc.)

5. **Hough Line Transform**
   - Detects straight line segments

6. **Lane Averaging & Extrapolation**
   - Combines detected segments into smooth lane boundaries

## Parameter Settings

| Parameter | Value |
|-----------|--------|
| Canny Thresholds | 50 / 150 |
| ROI | Lower 60% of frame |
| Slope Filter | \|m\| > 0.5 |
| Min Line Length | 40 px |


## Performance Evaluation

Tested on:

- **Processor:** AMD Ryzen 7 5700U  
- **RAM:** 16 GB  
- **OS:** 64-bit  

Results:

- Successful detections: **87%**
- Processing speed: **38 FPS**
- Frames tested: **500+**

## Limitations

- Heavy shadows
- Worn or faded lane markings
- Strong illumination changes
- Reduced performance in extreme weather

## Future Work

- Improve robustness under varying lighting and weather
- Support curved and multi-lane roads
- Add temporal smoothing and lane tracking
- Compare with deep learning–based methods

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/CharanjitBK/Autonomous-Lane-Detection.git 
   
Open the notebook in Google Colab/Jupyter.

## Acknowledgements

This project was inspired by and references the Udacity Self‑Driving Car Nanodegree Project 1: *Finding Lane Lines on the Road*.  
Original repository: [udacity/CarND-LaneLines-P1](https://github.com/udacity/CarND-LaneLines-P1)
