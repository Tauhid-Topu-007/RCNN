# 🐠 Aquarium Object Detection Dataset Analysis

A comprehensive analysis and visualization project for the Aquarium Object Detection dataset using COCO annotations. This project explores the dataset structure, visualizes bounding boxes with class labels, and provides insights into the aquarium species distribution.

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Dataset](#-dataset)
- [Technology Stack](#-technology-stack)
- [Installation](#-installation)
- [Dataset Structure](#-dataset-structure)
- [Data Analysis](#-data-analysis)
- [Visualization](#-visualization)
- [Code Implementation](#-code-implementation)
- [Results](#-results)
- [Project Structure](#-project-structure)
- [Troubleshooting](#-troubleshooting)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

---

## 🎯 Overview

This project provides tools and utilities for analyzing the Aquarium Object Detection dataset. It includes functionality for loading COCO-format annotations, visualizing images with bounding boxes and class labels, and exploring the dataset structure without requiring the pycocotools library.

---

## ✨ Features

- **Custom COCO Parser**: Parse COCO JSON annotations without external dependencies
- **Bounding Box Visualization**: Display images with class-labeled bounding boxes
- **Dataset Statistics**: Analyze class distribution and image counts
- **Flexible Visualization**: View random or specific images with annotations
- **No External Dependencies**: Uses only standard Python libraries
- **Google Colab Support**: Optimized for running in Colab environment

---

## 📊 Dataset

### Aquarium Dataset

- **Source**: [Kaggle - Aquarium Dataset](https://www.kaggle.com/datasets/sharansmenon/aquarium-dataset)
- **Total Images**: 832 (Training, Validation, Test split)
- **Classes**: 8 marine species
- **Format**: COCO JSON annotations

### Dataset Classes

| Class ID | Class Name | Supercategory |
|----------|------------|---------------|
| 0 | creatures | none |
| 1 | fish | creatures |
| 2 | jellyfish | creatures |
| 3 | penguin | creatures |
| 4 | puffin | creatures |
| 5 | shark | creatures |
| 6 | starfish | creatures |
| 7 | stingray | creatures |

---

## 🛠️ Technology Stack

| Category | Technologies |
|----------|--------------|
| **Language** | Python 3.7+ |
| **Data Processing** | JSON, OS |
| **Image Processing** | PIL/Pillow |
| **Visualization** | Matplotlib |
| **Environment** | Google Colab, Jupyter Notebook |

---

## 📦 Installation

### Option 1: Google Colab

```python
# Install dependencies
!pip install matplotlib pillow

# Clone repository or upload notebook
!git clone <repository-url>
cd <project-directory>
