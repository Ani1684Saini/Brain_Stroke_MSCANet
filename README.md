# Brain_SLGA_Net
A Scale-aware Local–Global Attention-Guided Network for Advancing Stroke Lesion Segmentation in Brain MRI. This repository contains the implementation of the SLGA-Net: Scale-aware Local–Global Attention-Guided Network Architecture, as described in our paper. The model is designed for the implementation of semantic segmentation to automatically detect brain stroke lesions from MRI scans. The project focuses on enhancing lesion localization and boundary delineation using deep learning architectures such as SLGA-Net and attention-enhanced hybrid models.

Instructions: Clone the repository: git clone https://github.com/Ani1684Saini/Brain_SLGA_Net

# Dataset Preparation
Dataset: Ischemic Stroke Lesion Segmentation Challenge - ISLES'22 - This challenge task aims to benchmark infarct segmentation in acute and sub-acute stroke using multimodal MRI data, namely DWI, ADC and FLAIR images. This challenge task aims to benchmark infarct segmentation in acute and sub-acute stroke using multimodal MRI data, including DWI, ADC, and FLAIR images. In this study, however, our experiments are conducted exclusively using diffusion-weighted imaging (DWI) MRI data. This multi-center dataset consists of 250 expert-annotated magnetic resonance imaging stroke cases. It is the training dataset for the Ischemic Stroke Lesion Segmentation Challenge (ISLES'22).
Dataset download link: The ISLES'22 train data can be downloaded from here:
https://zenodo.org/record/7960856#.ZK5or-xBzmE

Modalities used: DWI (only)

# Training and Evaluation Pipeline
The Train_and_Test folder contains scripts for training, validation, and testing the proposed segmentation model.
Purpose:
Dataset loading and preprocessing
Model training and validation
Performance evaluation on test data

# Preprocessing Steps: 
(1) Skull stripping (if required)
(2) Intensity normalization (Z-score)
(3) Slice extraction (axial)
(4) Resize to 128 × 128
(5) Subject-wise split (no data leakage)

# Network Architecture
The model folder contains a script that defines the deep learning architecture used for brain lesion segmentation.
Purpose: (1) Implements the proposed SLGA-Net model
(2) Defines encoder, decoder, and attention blocks

# Loss Functions and Metrics
The loss folder contains a script for custom loss functions and evaluation metrics tailored for brain stroke lesion segmentation.

# Implementation Flow
The complete implementation of the proposed SLGA-Net model is provided in a Jupyter Notebook (.ipynb), which serves as a self-contained and executable record of the experiments. All preprocessing steps, model definitions, training parameters, and evaluation procedures are explicitly defined within the notebook cells, allowing users to follow the experimental workflow sequentially. This notebook-based structure enables transparent inspection of intermediate outputs, parameter settings, and results at each stage of execution.
The implementation begins with dataset loading and preprocessing, including resizing, normalization, and subject-wise splitting to prevent data leakage. The model architecture is then constructed using modular components defined in the model directory, while custom loss functions and evaluation metrics are imported from the loss directory. Training and validation are performed within the notebook using clearly defined hyperparameters, and the best-performing model is saved for subsequent evaluation. Final testing and inference are conducted on unseen data, with both quantitative metrics and qualitative segmentation results reported directly in the notebook.

# Requirements
All experiments were conducted using Python version 3.10.1 and TensorFlow version 2.10.1. The complete list of required Python packages and their corresponding versions is provided in the requirements.txt file to ensure a consistent software environment. Installing the dependencies listed in this file ensures compatibility with the implemented model, training pipeline, and evaluation procedures, thereby facilitating the accurate replication of the reported results.
