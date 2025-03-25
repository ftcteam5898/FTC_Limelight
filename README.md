# FTC Limelight Detection Model Training

This repository contains a modified version of the official Limelight Vision object detection training notebook, specifically adapted for Kaggle environments rather than Google Colab.

## Overview

The Limelight Vision system is commonly used in FIRST Tech Challenge (FTC) competitions for computer vision and object detection tasks. This project provides tools to train custom detection models that can be deployed to Limelight hardware.

## Features

- Train custom object detection models for FTC game elements
- Supports TensorFlow 2.x with SSD MobileNet v2 architecture
- Generates optimized TFLite models compatible with Limelight hardware
- Includes quantized models (8-bit) and Google Coral TPU optimized versions
- Kaggle-specific adaptations for better performance and compatibility

## Requirements

- Kaggle notebook environment with GPU acceleration
- TensorFlow 2.15
- Python 3.10+
- Dataset in TFRecord format (can be created using tools like Roboflow)

## Setup Instructions

1. Create a new Kaggle notebook
2. Upload the `limelight-detection.ipynb` notebook
3. Enable GPU acceleration in Kaggle notebook settings
4. Run the cells in sequence

## Dataset Preparation

Your dataset should be prepared in TFRecord format with the following structure:
- Train folder with training examples and label map
- Valid folder with validation examples
- Test folder (optional)

## Training Process

The notebook guides you through:
1. Installing the TensorFlow Object Detection API
2. Setting up the training environment
3. Loading and analyzing your dataset
4. Configuring the model
5. Training the model
6. Converting to TFLite format
7. Quantizing for better performance
8. Compiling for Google Coral TPU (used in Limelight hardware)

## Outputs

After training completes, the notebook will generate:

- Full TensorFlow saved model
- 32-bit TFLite model (highest accuracy)
- 8-bit quantized TFLite model (better performance)
- Google Coral TPU optimized model (for Limelight hardware)
- Labels file

## Differences from Official Version

This adaptation differs from the official Limelight training notebook in these ways:
- Configured specifically for Kaggle rather than Google Colab
- Fixed compatibility issues with TensorFlow 2.15
- Modified paths and environment variables for Kaggle
- Improved error handling and progress reporting
- Added pre-training dataset validation

## Acknowledgements

This project is adapted from the official Limelight Vision training notebook with modifications for Kaggle compatibility.

## License

Please refer to the original Limelight Vision license for usage terms.
