# Brain_SLGA_Net
A Scale-aware Local–Global Attention-Guided Network for Advancing Stroke Lesion Segmentation in Brain MRI. This repository contains the implementation of the SLGA-Net: Scale-aware Local–Global Attention-Guided Network Architecture, as described in our paper. The model is designed for the implementation of semantic segmentation to automatically detect brain stroke lesions from MRI scans. The project focuses on enhancing lesion localization and boundary delineation using deep learning architectures such as SLGA-Net and attention-enhanced hybrid models.

Instructions: Clone the repository: git clone https://github.com/Ani1684Saini/Brain_SLGA_Net

# Dataset Preparation
Dataset: Ischemic Stroke Lesion Segmentation Challenge - ISLES'22 - This challenge task aims to benchmark infarct segmentation in acute and sub-acute stroke using multimodal MRI data, namely DWI, ADC and FLAIR images. This challenge task aims to benchmark infarct segmentation in acute and sub-acute stroke using multimodal MRI data, including DWI, ADC, and FLAIR images. In this study, however, our experiments are conducted exclusively using diffusion-weighted imaging (DWI) MRI data. This multi-center dataset consists of 250 expert-annotated magnetic resonance imaging stroke cases. It is the training dataset for the Ischemic Stroke Lesion Segmentation Challenge (ISLES'22).
Dataset download link: The ISLES'22 train data can be downloaded from here:
https://zenodo.org/record/7960856#.ZK5or-xBzmE

Modalities used: DWI (only)

Preprocessing Steps: 
1 Skull stripping (if required)
2 Intensity normalization (Z-score)
3 Slice extraction (axial)
4 Resize to 128 × 128
5 Subject-wise split (no data leakage)

Requirements: Python version 3.10.12, TensorFlow version 2.10.0 
