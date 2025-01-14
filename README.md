# Object and Sub-Object Detection System

## Overview
This project implements a two-level detection system using YOLOv8 to identify main objects (e.g., cars, bikes) and their sub-components (e.g., wheels, headlights). The system is designed for detailed scene understanding, enabling granular analysis for applications in industries like automotive, manufacturing, and robotics.

## System Features
- **Main Object Detection**: Uses YOLOv8 pretrained weights for high-accuracy detection of main objects.
- **Sub-Object Detection**: Fine-tuned YOLOv8 model for detecting sub-components within main objects.
- **Optimizations**: Reduced frame size and lightweight models ensure reasonable inference times on a CPU.

## Hardware Requirements
- **CPU**: Tested on a MacBook Air with an M1 chip.
- **RAM**: Minimum 8 GB recommended.
- **OS**: macOS or any Linux distribution.

## Software Requirements
- Python 3.8 or above
- Required Python libraries (listed in `requirements.txt`):
  - PyTorch
  - Ultralytics (YOLOv8)
  - OpenCV
  - NumPy
  - Roboflow (if using dataset APIs)

## Dataset Preparation
1. Organize the dataset as follows:
   ```
   dataset/
     ├── train/
     │   ├── images/
     │   ├── labels/
     ├── valid/
     │   ├── images/
     │   ├── labels/
   ```
2. Ensure images and labels are in YOLO format.
3. If using Roboflow, export the dataset and place it in the `dataset` folder.

## Running the System
### Step 1: Main Object Detection
Run the pretrained YOLOv8 model to detect main objects:


### Step 2: Sub-Object Detection
Use the fine-tuned YOLOv8 model to detect sub-objects:


### Step 3: Combined Detection Pipeline
Run the complete detection pipeline:

## Reproducing Results
1. Fine-tune YOLOv8 on the custom sub-object dataset:
   
2. Evaluate the fine-tuned model:
 
3. Compare metrics (e.g., precision, recall, mAP) with those documented in the report.

## Optimizations
- **Reduced Frame Size**: Resizing input frames improved inference speed without significant accuracy loss.
- **Batch Processing**: Used during validation to optimize CPU utilization.

## Troubleshooting
- If models fail to load, ensure correct paths to `.pt` files are provided.
- For issues with dataset loading, verify the dataset structure and annotation format.

## Future Work
- Extend the dataset for better generalization.
- Optimize for real-time applications on edge devices.
- Can be further optimized for better fps.

## Contact
For further assistance, please reach out to:
- Pavan Sai
- Email: pavansai.bheemisetty@gmail.com
- GitHub: https://github.com/PavansaiBheemisetty


