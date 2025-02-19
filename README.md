# Multiscale-Vision-Mamba-Unet-for-Tumor-Segmentation-on-Breast-Ultrasound-Images

## Individual role
  _As the primary contributor to this project, I was responsible for the conceptualization, model development, and implementation of the InViM-UNet architecture. My key responsibilities included: formulating the initial idea, designing and coding the model, integrating the Inception Module, select the appropriate module structure and location to integrate into the model, conducting experiments, selecting optimal parameters, and writing the paper for submission._

## Project Goals

**Problem Statement:**

*   Difficulty in accurately segmenting breast tumors in ultrasound images due to variability in shape and size.

*   Existing segmentation methods struggle with diverse tumor characteristics.

**Importance:**

*   Early breast cancer detection improves recovery rates.

*   Accurate ultrasound tumor segmentation is crucial for reliable diagnosis.

**Specific Objectives:**

*   To develop an enhanced segmentation model, "Inception Vision Mamba U-Net (InViM-UNet)," specifically designed to address the challenges of segmenting breast tumors in ultrasound images with varied shapes and sizes.

*   To integrate the Inception Module into the Vision Mamba U-Net architecture to capture multi-scale features effectively.

*   To outperform existing state-of-the-art models in breast tumor segmentation accuracy.

**Target Audience:**

*   Radiologists, oncologists, and medical professionals involved in breast cancer diagnosis and treatment.

## Methodology

**Architectural Components:**

*   Vision Mamba U-Net (ViM-UNet) architecture: A U-Net based model using Visual State Space (VSS) blocks and simple skip connections.

*   Inception Module: Integrated immediately after the patch embedding layer to capture multi-scale features.

*   Asymmetric convolutions: Employed in the Inception Module to enhance efficiency and reduce complexity.

**Why were these methods chosen?**

*   ViM-UNet: Provides good efficiency and leverages SSMs for long-range dependencies.

*   Inception Module: Effective at capturing information at different scales by employing parallel convolutional filters with varying kernel sizes within a single layer. This is important for handling tumor diversity.

*   Asymmetric Convolutions: Reduces computational complexity while maintaining multi-scale feature extraction.

**Were there any modifications or improvements made?**

*   The Inception Module was strategically placed immediately after the patch embedding layer, rather than within the network like in other architectures.

*   The standard Inception module was modified to incorporate asymmetric convolutions for enhanced efficiency.

**Dataset:**

*   Utilized the Breast Ultrasound Dataset.

*   Contains images with annotation, having undergone image process (e.g remove boundaries, conversion from DICOM to PNG format...)

*   Training & Evaluation Procedure:

*   Model Training using Ultrasound Dataset, focusing on loss metrics and validation techniques.

*   Comparison with baseline segmentation models to validate InViM-UNet improvement.

## Results

**Evaluation Metrics:**

*   Dice Score (Similarity between predicted and ground truth segmentations).

*   Precision (Accuracy of positive predictions).

*   Recall (Ability to capture all positive cases).

*   F1-Score (Harmonic mean of Precision and Recall).

*   IoU (Intersection over Union) – (Overlap between predicted and ground truth segmentations).

**Key Performance Achieved:**

*   InViM-UNet achieved the best overall performance with a Dice score of 0.7809, Precision of 0.9240, F1-Score of 0.7912, and IoU of 0.6889.

**Comparative Analysis:

*   InViM-UNet significantly outperformed other models including ViM-UNet, UNet, MSVM-UNet, and ViT+UNet based on metrics like Dice score and IoU.

 
