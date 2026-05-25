# Transformer-Augmented Dual Decoder Framework for Brain Lesion Image Segmentation

A deep learning-based medical image segmentation framework for ischemic stroke lesion segmentation using diffusion-weighted MRI (DWI-MRI) images. The proposed architecture integrates a Transformer bottleneck within a dual-decoder U-Net framework for simultaneous lesion region and boundary prediction.

---

## Overview

This project focuses on automated ischemic stroke lesion segmentation using a boundary-aware CNN-Transformer architecture. The framework combines:

- CNN-based local feature extraction
- Transformer-based global contextual learning
- Dual-decoder segmentation and boundary prediction
- Signed Distance Function (SDF)-based supervision
- Dynamic multi-task loss optimization

The model is designed to improve lesion contour localization and structural consistency in challenging MRI segmentation scenarios.

---

## Architecture

The proposed framework consists of:

### Encoder
- Convolutional blocks
- Batch normalization
- ReLU activation
- Spatial dropout
- Max pooling

### Transformer Bottleneck
- Positional embeddings
- Multi-head self-attention
- Feed Forward Network (FFN)
- Residual connections
- Layer normalization

### Dual Decoders

#### Segmentation Decoder
Predicts lesion segmentation masks.

#### Boundary Decoder
Predicts lesion boundary representations using boundary-aware supervision.

---

## Key Features

- Transformer-enhanced U-Net architecture
- Dual-decoder framework
- Boundary-aware segmentation
- Signed Distance Function (SDF) learning
- Dynamic loss weighting
- Mixed precision training
- Slice-wise MRI processing pipeline
- Patient-wise dataset splitting

---

## Dataset

The framework uses the ISLES’22 (Ischemic Stroke Lesion Segmentation 2022) dataset.

Dataset characteristics:
- Diffusion-weighted MRI (DWI)
- NIfTI (.nii.gz) format
- Expert-annotated lesion masks
- Multi-center ischemic stroke dataset

---

## Preprocessing

The preprocessing pipeline includes:

- Slice-wise extraction from 3D MRI volumes
- Lesion-only slice filtering
- Min-max normalization
- Image resizing/padding to 128×128
- Data augmentation:
  - Horizontal flip
  - Vertical flip
  - Rotation

---

## Loss Functions

The framework uses multi-task optimization:

### Segmentation Loss
- Dice Loss

### Boundary Loss
- Binary Cross-Entropy (BCE)
- Signed Distance Function (SDF)-based supervision

### Total Loss
Dynamic weighted combination of segmentation and boundary losses.

---

## Evaluation Metrics

The model is evaluated using:

- Dice Coefficient
- Intersection over Union (IoU)
- Hausdorff Distance
- Precision
- Recall

---

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- OpenCV
- NiBabel
- Scikit-learn
- Matplotlib

---

## Project Structure

├── dataset/
├── models/
├── preprocessing/
├── training/
├── evaluation/
├── visualization/
├── notebooks/
├── results/
├── README.md
└── requirements.txt

---

## Installation

git clone https://github.com/your-username/Transformer-DualDecoder-BrainLesionSegmentation.git

cd Transformer-DualDecoder-BrainLesionSegmentation

Install dependencies:

pip install -r requirements.txt

---

## Training

Run the training script:

python train.py

---

## Testing

Run inference and evaluation:

python test.py

---

## Results

The proposed framework demonstrates effective lesion segmentation and improved boundary localization through:
- Transformer-based contextual learning
- Boundary-aware supervision
- Multi-task optimization

---

## Applications

- Ischemic stroke lesion segmentation
- Medical image analysis
- MRI-based clinical assistance
- Boundary-aware medical segmentation research

---

## Future Work

- Multi-modal MRI integration
- Lightweight Transformer architectures
- 3D volumetric segmentation
- Cross-dataset generalization
- Real-time clinical deployment

---

## Citation

@project{brainlesionsegmentation2026,
  title={Transformer-Augmented Dual Decoder Framework for Brain Lesion Image Segmentation},
  author={Ashish Das},
  year={2026}
}

---

## Author

Ashish Das
Department of Computer Science and Engineering
National Institute of Technology Rourkela
