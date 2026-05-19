# Facial Emotion Recognition using Vision Transformer (ViT)

## Overview

This project presents a high-performance **Facial Emotion Recognition system** built using a custom **Vision Transformer (ViT)** architecture trained on the large-scale **FER2025** dataset.  
The model is capable of classifying human facial expressions into 7 emotional categories:

- Angry
- Disgust
- Fear
- Happy
- Neutral
- Sad
- Surprise

The entire deep learning pipeline was implemented in **PyTorch** and optimized for large-scale training using modern computer vision and transformer-based techniques.

Unlike traditional CNN-based approaches, this implementation uses a fully custom Vision Transformer architecture with transformer encoder blocks, patch embeddings, positional encoding, mixed precision training, advanced augmentation strategies, checkpointing, fine-tuning, and detailed evaluation metrics.

---

# Results

## Final Performance

| Metric | Score |
|---|---|
| Test Accuracy | **91.91%** |
| Macro F1-Score | **0.9186** |
| Precision | **0.9188** |
| Recall | **0.9187** |

The model achieved strong and balanced performance across all 7 emotion classes on a test set containing over **238,000 images**.

---

# Dataset

## FER2025 Dataset

The project uses the **FER2025** dataset downloaded directly from HuggingFace.

### Dataset Statistics

| Split | Images |
|---|---|
| Training Images | **1,351,613** |
| Testing Images | **238,197** |

### Emotion Classes

- angry
- disgust
- fear
- happy
- neutral
- sad
- surprise

A deterministic hash-based split strategy was implemented to ensure reproducibility and consistency between training and testing data.

---

# Model Architecture

## Custom Vision Transformer (ViT)

The architecture was implemented entirely from scratch using PyTorch components.

### Main Components

- Patch Embedding Layer
- Positional Encoding
- Multi-Head Self Attention
- Transformer Encoder Blocks
- Layer Normalization
- GELU Activation
- Classification Head

### Configuration

| Parameter | Value |
|---|---|
| Image Size | 48x48 |
| Patch Size | 4 |
| Embedding Dimension | 256 |
| Attention Heads | 4 |
| Transformer Depth | 6 |
| MLP Dimension | 512 |
| Dropout | 0.10 |
| Batch Size | 64 |
| Epochs | 47 |

---

# Training Pipeline

The training process includes several optimization techniques used in modern production-grade deep learning systems.

## Features

- Mixed Precision Training (AMP)
- Gradient Clipping
- AdamW Optimizer
- ReduceLROnPlateau Scheduler
- Label Smoothing
- Fine-Tuning Stage
- Automatic Checkpoint Saving
- Validation Monitoring
- Resume Training Support

---

# Image Preprocessing & Augmentation

The pipeline includes multiple augmentation techniques to improve generalization and robustness.

## Augmentations Used

- Grayscale Conversion
- Resize
- Random Horizontal Flip
- Random Autocontrast
- Random Equalization
- Random Affine Transformations
- Random Erasing
- Normalization

---

# Visualizations

The notebook includes detailed visual analysis and monitoring:

- Original vs Augmented Images
- Dataset Distribution
- Pixel Intensity Histograms
- Confusion Matrix
- Training vs Validation Accuracy
- Training vs Validation Loss
- F1-Score Evolution
- Per-Class Performance
- Correct / Incorrect Prediction Examples

---

# Technologies Used

## Deep Learning & AI

- PyTorch
- Torchvision
- Vision Transformers (ViT)
- Scikit-learn

## Data & Visualization

- NumPy
- Matplotlib

## Dataset & Infrastructure

- HuggingFace Hub
- Google Colab
- Google Drive

---

# Project Structure

```bash
EmotionDetection-ViT-FER2025/
│
├── EmotionDetection4.ipynb
├── emotiondetection4.py
├── README.md
│
├── results/
│   ├── confusion_matrix.png
│   ├── training_curves.png
│   └── sample_predictions.png
│
└── models/
    └── best_vit_model.pth
```

---

# Key Highlights

- Custom Vision Transformer implementation from scratch
- Large-scale dataset with over 1.5 million images
- Production-style training pipeline
- High test accuracy (~91.9%)
- Strong macro F1-score performance
- Advanced augmentation and optimization techniques
- Full evaluation and visualization suite
- Scalable and reproducible workflow

---

# Future Improvements

Possible future extensions include:

- Real-time webcam emotion recognition
- Deployment with FastAPI or Flask
- ONNX / TensorRT optimization
- Mobile deployment
- Attention map visualization
- Hybrid CNN + Transformer architectures
- Explainable AI integration

---

# Author

**Oana Ilies**  
Master's Student – Multimedia Technologies  
Technical University of Cluj-Napoca (UTCN)

Passionate about:
- Artificial Intelligence
- Deep Learning
- Computer Vision
- Intelligent Systems
- AI Automation
