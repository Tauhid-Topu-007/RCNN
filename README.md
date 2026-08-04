# 🐠 Aquarium Object Detection using Faster R-CNN

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/aquarium-object-detection/blob/main/aquarium_detection.ipynb)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-ee4c2c.svg)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## Overview

This project implements an object detection pipeline to identify and classify marine life in aquarium images. Using a Faster R-CNN model with a MobileNetV3 backbone, the system can detect multiple aquatic creatures including fish, jellyfish, penguins, puffins, sharks, and starfish in a single image. The model leverages transfer learning from a pre-trained COCO checkpoint.

---

## Features

- **Data Pipeline**: Custom PyTorch Dataset class handling COCO-format annotations
- **Augmentation**: Dynamic image transformations using albumentations library
- **Transfer Learning**: Pre-trained fasterrcnn_mobilenet_v3_large_fpn backbone
- **Performance Tracking**: Detailed loss logging for each training component
- **GPU Support**: Optimized for CUDA-enabled GPUs
- **Visualization**: Side-by-side comparison of original images with predictions

---

## Dataset

This project uses the **Aquarium Combined** dataset from Kaggle.

| Attribute | Description |
|-----------|-------------|
| Source | [Aquarium Dataset](https://www.kaggle.com/datasets/sharansmenon/aquarium-dataset) |
| Classes | fish, jellyfish, penguin, puffin, shark, starfish, stingray |
| Format | COCO JSON format |
| Splits | Train, Validation, Test |

---

## Model Architecture

The model uses **Faster R-CNN** with a MobileNetV3-Large backbone.

| Component | Description |
|-----------|-------------|
| Backbone | fasterrcnn_mobilenet_v3_large_fpn (pre-trained on COCO) |
| Custom Head | Replaced predictor to match 7 classes |
| Total Parameters | ~18.9M |
| Trainable Parameters | ~18.8M |

---

## Installation

### Prerequisites
- Python 3.8+
- CUDA-capable GPU (recommended)
- Kaggle API key

### Steps

```bash
# Clone repository
git clone https://github.com/your-username/aquarium-object-detection.git
cd aquarium-object-detection

# Install dependencies
pip install -r requirements.txt

# Download dataset
mkdir ~/.kaggle
cp kaggle.json ~/.kaggle/
kaggle datasets download sharansmenon/aquarium-dataset
unzip aquarium-dataset.zip -d ./data/
