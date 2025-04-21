# 🖼️ Image Super-Resolution using FSRCNN

This project implements a deep learning-based image super-resolution system using the **Fast Super-Resolution Convolutional Neural Network (FSRCNN)**. The goal is to upscale low-resolution images while recovering high-frequency details in an efficient and visually pleasing way.

## 📌 Project Overview

Super-resolution (SR) is the task of reconstructing high-resolution (HR) images from their low-resolution (LR) counterparts. This project uses FSRCNN — an optimized architecture designed for both speed and quality — to enhance image details while maintaining real-time performance.

This work was completed as part of the graduate course project in **EE8204 - Neural Networks** at Toronto Metropolitan University.

## 🧠 Model Architecture

The FSRCNN model consists of:
* **Feature Extraction** (`5×5 conv`)
* **Shrinking** (`1×1 conv`)
* **Non-linear Mapping** (`3×3 conv × m`)
* **Expanding** (`1×1 conv`)
* **Deconvolution (Upsampling)** using `sub-pixel shuffling`

Model parameters:
* `scale factor`: 2×
* `d = 48`, `s = 10`, `m = 3` (custom-reduced from the original FSRCNN paper)

## 🗂️ Dataset

We use the DIV2K dataset for training and evaluation:
* 800 images for training
* 100 for validation
* 100 for testing
* Bicubic downsampled at ×2

## 📈 Results

Quantitative Metrics on Test Set:
* **PSNR**: 30.73 dB
* **SSIM**: 0.82
* **MSE**: 0.0021

Training Curves:

[Insert training curves image here]

Visual Comparisons:
- FSRCNN Output vs Ground Truth [Insert comparison image here]
- Input vs Ground Truth (No SR) [Insert comparison image here]

## ⚙️ Training Details

* Optimizer: `Adam` (LR = 0.001)
* Loss: `Mean Squared Error` 
* Metrics: `PSNR`, `SSIM`
* Epochs: 50
* Batch Size: 32
* Callbacks: `ReduceLROnPlateau`, `EarlyStopping`, and `ModelCheckpoint`

## 📄 Report

For detailed methodology, citations, and results, refer to the 📘 [Final Report (PDF)](link-to-your-report.pdf).

## 🚀 Future Work

* Incorporate **VGG-based perceptual loss** for sharper outputs
* Experiment with **residual or attention blocks**
* Adapt FSRCNN for domain-specific tasks (e.g. medical imaging, satellite)

## 🧑‍💻 Author

**Samin Razeghi**  
M.Eng. in Computer Engineering, AI Specialization  
# 🖼️ Image Super-Resolution using FSRCNN

This project implements a deep learning-based image super-resolution system using the **Fast Super-Resolution Convolutional Neural Network (FSRCNN)**. The goal is to upscale low-resolution images while recovering high-frequency details in an efficient and visually pleasing way.

## 📌 Project Overview

Super-resolution (SR) is the task of reconstructing high-resolution (HR) images from their low-resolution (LR) counterparts. This project uses FSRCNN — an optimized architecture designed for both speed and quality — to enhance image details while maintaining real-time performance.

This work was completed as part of the graduate course project in **EE8204 - Neural Networks** at Toronto Metropolitan University.

## 🧠 Model Architecture

The FSRCNN model consists of:
* **Feature Extraction** (`5×5 conv`)
* **Shrinking** (`1×1 conv`)
* **Non-linear Mapping** (`3×3 conv × m`)
* **Expanding** (`1×1 conv`)
* **Deconvolution (Upsampling)** using `sub-pixel shuffling`

Model parameters:
* `scale factor`: 2×
* `d = 48`, `s = 10`, `m = 3` (custom-reduced from the original FSRCNN paper)

## 🗂️ Dataset

We use the DIV2K dataset for training and evaluation:
* 800 images for training
* 100 for validation
* 100 for testing
* Bicubic downsampled at ×2

## 📈 Results

Quantitative Metrics on Test Set:
* **PSNR**: 30.73 dB
* **SSIM**: 0.82
* **MSE**: 0.0021

Training Curves:

[Insert training curves image here]

Visual Comparisons:
- FSRCNN Output vs Ground Truth [Insert comparison image here]
- Input vs Ground Truth (No SR) [Insert comparison image here]

## ⚙️ Training Details

* Optimizer: `Adam` (LR = 0.001)
* Loss: `Mean Squared Error` 
* Metrics: `PSNR`, `SSIM`
* Epochs: 50
* Batch Size: 32
* Callbacks: `ReduceLROnPlateau`, `EarlyStopping`, and `ModelCheckpoint`

## 📄 Report

For detailed methodology, citations, and results, refer to the 📘 [Final Report (PDF)](link-to-your-report.pdf).

## 🚀 Future Work

* Incorporate **VGG-based perceptual loss** for sharper outputs
* Experiment with **residual or attention blocks**
* Adapt FSRCNN for domain-specific tasks (e.g. medical imaging, satellite)

## 🧑‍💻 Author

**Samin Razeghi**  
M.Eng. in Computer Engineering, AI Specialization  
📧 samin.razeghi@torontomu.ca

## 📚 References

Key sources include:
* Dong et al., *"Fast and Accurate Image Super-Resolution with Deep Convolutional Networks"*, TPAMI 2016.
* Agustsson and Timofte, *"NTIRE 2017 Challenge"*, CVPR 2017.
* Ledig et al., *"Photo-Realistic SR Using GANs"*, CVPR 2017.

(Full list in the report).

## 📚 References

Key sources include:
* Dong et al., *"Fast and Accurate Image Super-Resolution with Deep Convolutional Networks"*, TPAMI 2016.
* Agustsson and Timofte, *"NTIRE 2017 Challenge"*, CVPR 2017.
* Ledig et al., *"Photo-Realistic SR Using GANs"*, CVPR 2017.

(Full list in the report).
