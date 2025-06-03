# Identifying_Banned_Individuals

# Surveillance Software for Identifying Banned Individuals in Feeds

## Overview

This project implements a smart surveillance system designed to automatically detect and identify banned individuals from both pre-recorded surveillance videos and real-time camera feeds. It combines deep learning-based face recognition techniques with efficient video processing to provide real-time alerts and visual confirmation.

## Features

- Face detection in video frames using Haar Cascade or MTCNN  
- Embedding generation using MobileNetV2, ResNet50, and EfficientNetB0  
- Cosine similarity-based face matching  
- Real-time alerting system with timestamps and face image snapshots  
- Visual verification using side-by-side comparison  
- Modular design for future upgrades (e.g., model replacement, live dashboards)

## System Architecture

1. **Input**: Pre-recorded video or live camera feed  
2. **Face Detection**: Haar Cascade or MTCNN  
3. **Face Embedding**: MobileNetV2 (default), ResNet50, EfficientNetB0  
4. **Similarity Check**: Cosine similarity with a threshold (0.77)  
5. **Alert Generation**: Cropped image, timestamp, matched identity  
6. **Visualization**: Matplotlib module for side-by-side comparisons  

## Dataset

- **Source**: [VGGFace2 Dataset](https://www.robots.ox.ac.uk/~vgg/data/vgg_face2/)  
- **Subset Used**: A curated blacklist of banned individuals  
- **Split**:
  - 80% training  
  - 20% validation  

## Models Used

| Model          | Validation Accuracy | Validation Loss |
|----------------|---------------------|-----------------|
| MobileNetV2    | 75.44%              | 0.9437          |
| ResNet50       | 9.27%               | 4.4146          |
| EfficientNetB0 | 32.00%              | 3.7320          |

## Evaluation Metrics

- Accuracy  
- Precision  
- Recall  
- F1 Score  
- ROC-AUC Curve  
- Confusion Matrix  

## Sample Outputs

- Red bounding box around detected face  
- Side-by-side comparison with matched banned individual  
- Cosine similarity score for verification  

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/surveillance-face-recognition.git
   cd surveillance-face-recognition
