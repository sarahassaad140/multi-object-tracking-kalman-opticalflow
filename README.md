# Multi-Object Tracking using Kalman Filter and Optical Flow

## Overview

This project implements a Multi-Object Tracking (MOT) system capable of tracking multiple pedestrians across video sequences while maintaining object identities over time.

The system combines classical computer vision techniques including Kalman Filtering, Optical Flow, IoU-based matching, and the Hungarian Assignment Algorithm to achieve reliable tracking performance without relying on deep learning detectors.

---

## Objectives

* Detect and track multiple moving objects
* Maintain consistent object identities
* Predict object motion across frames
* Visualize trajectories and movement patterns
* Evaluate tracking performance using MOT metrics

---

## Dataset

### MOT15 Challenge Dataset

Sequence Used:

* ADL-Rundle-6

Dataset Components:

* Video frames
* Detection annotations
* Ground-truth annotations

---

## Methodology

### 1. Detection Loading

Object detections are loaded frame-by-frame from the MOT15 dataset.

### 2. Kalman Filter Prediction

A constant-velocity Kalman Filter predicts future object positions and handles temporary missed detections.

### 3. Optical Flow Refinement

Lucas-Kanade Optical Flow estimates motion between consecutive frames and improves prediction stability.

### 4. IoU Computation

Intersection-over-Union (IoU) is used to measure similarity between detections and predicted bounding boxes.

### 5. Hungarian Matching

The Hungarian Algorithm performs optimal assignment between detections and tracked objects.

### 6. Visualization

The system generates:

* Bounding boxes
* Object IDs
* Motion trajectories
* Tracking videos
* Trajectory maps

---

## Technologies Used

* Python
* OpenCV
* NumPy
* SciPy
* FilterPy

---

## Computer Vision Concepts

* Multi-Object Tracking (MOT)
* Kalman Filtering
* Lucas-Kanade Optical Flow
* Data Association
* IoU Matching
* Hungarian Algorithm
* Motion Prediction
* Object Re-Identification

---

## Results

### Tracking Performance

| Metric          | Value  |
| --------------- | ------ |
| MOTA            | 36.47% |
| MOTP            | 72.20% |
| True Positives  | 2547   |
| False Positives | 667    |
| False Negatives | 2462   |
| ID Switches     | 53     |

The system successfully tracked multiple pedestrians while maintaining object identities and generating continuous trajectory visualizations.

---

## Outputs

* Tracked video visualization
* Trajectory maps
* MOT evaluation metrics
* Tracking result files
* Object movement analysis

---

## Skills Demonstrated

* Computer Vision
* Multi-Object Tracking
* Motion Estimation
* Kalman Filtering
* Optical Flow
* Algorithm Design
* Performance Evaluation
* OpenCV Development

---

## Future Improvements

* DeepSORT integration
* Appearance-based re-identification
* YOLO object detection
* GPU acceleration
* Real-time deployment
* Occlusion handling improvements

---

## Author

Sarah Assaad

Master's Student in Data Science & Artificial Intelligence

