# OCR Model Comparison: EasyOCR vs TesseractOCR

This repository provides a comparison of two popular Optical Character Recognition (OCR) models: EasyOCR and TesseractOCR. The comparison is based on resource consumption, speed, and accuracy using a dataset of 8 test images. 


The repository is structured around two main Jupyter notebooks:

Model Results: Showcases the OCR results for each model on the 8 test images.
Comparison: Provides a detailed comparison between the two models in terms of performance, resource consumption, and ease of use.

## Overview
This project compares two OCR models:

EasyOCR: A user-friendly, GPU-accelerated OCR library that supports more than 80 languages.
TesseractOCR: An open-source OCR engine that supports multiple languages, widely used and recognized for its simplicity.

## The key focus of the comparison includes:

Accuracy: How well each model extracts text from the provided images.
Speed: Time taken to process each image.
Resource Usage: CPU, Memory, and (for EasyOCR) GPU consumption during the OCR process.
Ease of Use: How easy it is to set up, integrate, and use each OCR model.

3# Installation
To run the notebooks, you need to set up the environment for both OCR models. Below are the instructions for installing both EasyOCR and Tesseract.

### EasyOCR Installation
``` pip install easyocr ```

### Tesseract Installation
1. First install model 
ex: for linux: ``` sudo apt install tesseract-ocr ```

2. After installing Tesseract, install the Python bindings:
``` pip install pytesseract ```

### Additional Dependencies
To ensure all dependencies are installed, use the following command:
``` pdm install ```

## Notebooks
### 1. Model Results
File: ocr_model_results.ipynb

This notebook demonstrates the results of each OCR model (EasyOCR and Tesseract) when applied to the 8 test images. For each image, both models are run, and their output text is displayed alongside the original image.

### 2. Comparison
File: ocr_model_comparison.ipynb

This notebook presents a detailed comparison between EasyOCR and TesseractOCR across the 8 test images. The comparison includes:

Speed: Measuring the time taken for each model to process the images.
Resource Consumption: Tracking memory, CPU, and GPU (for EasyOCR) usage during processing.

Key sections:
Measuring and comparing processing times for each model.
Tracking memory and CPU consumption using psutil.
(For EasyOCR) Measuring GPU usage using nvidia-smi.
Summary of results and analysis.

## Dataset
This repo use 8 text images for different cases to test each model under these case.
The cases are:
1. best case image
2. distorted text
3. tiny text
4. handwritten text
5. Mixed fonts text
6. low contrast text image
7. real photgraphed document 

Dependencies
The key dependencies for the project are:

- easyocr
- pytesseract
- scikit-image
- GPUtil
- psutil
- ipykernel
- Jupyter
- pandas
- matplotlib