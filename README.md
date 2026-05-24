# ML-Based-Surface-Roughness-Prediction-Model-Project
An end-to-end Machine Learning pipeline utilizing a ResNet50 Hybrid Regression model to predict the continuous surface roughness of aluminum microstructures. Features a full-stack Glassmorphism web interface built with Flask and Gradio.

Project Overview
This repository contains the complete codebase for the ML-Based Surface Roughness Prediction project developed during an IIT Bombay internship. The system is designed to automate and simplify the analysis of metal microstructures. It takes a microstructural image of an aluminum sample captured under a digital microscope and instantly predicts its continuous surface roughness value.

As manufacturing and materials engineering demand higher precision, this technology-driven inspection method empowers quality control engineers with rapid, non-destructive, and highly accurate mathematical estimations without the need for traditional physical measurements.

Key Features


Softmax-Hybrid Regression Architecture: The neural network was transitioned from a standard classification model to a highly accurate continuous hybrid regression model. It utilizes a custom mathematical Lambda layer to calculate expected values, outputting fluid, real-world decimals instead of static categories.


Advanced Data Pipeline: Implements a strict stratified data split to completely prevent data leakage.


Extreme Data Augmentation: Overcomes the constraints of a small original dataset by applying offline image augmentation (lossless multi-angle OpenCV rotations) alongside extreme online augmentation (dynamic flips, zooms, and brightness shifts during training).


Deep Neural Stabilizers: Integrates Batch Normalization, Dropout layers, and Huber Loss to help the ResNet50 model process and learn extremely microscopic target values (e.g., 0.033, 0.0667, 0.167).


Target Scaling Technique: Employs a mathematical scaling trick by multiplying target labels by 1000 during training and dividing the raw output by 1000 during inference to ensure high precision and prevent vanishing gradients.


Premium Web UI: The models are deployed into production-ready, interactive web interfaces featuring a modern "Glassmorphism" design.

Technology Stack


Deep Learning: Python, TensorFlow, Keras, ResNet50.


Computer Vision & Data Engineering: OpenCV (cv2), NumPy, Pandas, Scikit-Learn.


Frontend & Deployment: HTML, CSS, Flask, Gradio.


Environments: Google Colab (GPU Training) and VS Code (Web App Deployment).

Credits
Prepared by IIT Bombay Interns - Devraj Mane & Krutika Kamble.
