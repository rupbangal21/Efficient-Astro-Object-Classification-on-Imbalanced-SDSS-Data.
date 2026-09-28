# Efficient-Astro-Object-Classification-on-Imbalanced-SDSS-Data.
Swin Transformer-based classification of Galaxy, QSO, and Star objects using the SDSS17 dataset.

An AI-based astronomical object classification system that classifies celestial objects into Galaxy, Quasar (QSO), and Star categories using the Swin Transformer architecture.
The project uses the SDSS17 dataset and compares the performance of Swin Transformer, Vision Transformer (ViT), and Convolutional Neural Network (CNN) under the same experimental conditions. The Swin Transformer achieves an overall accuracy of 97.25% on the held-out test set.

📌 Overview

Modern astronomical surveys generate extremely large amounts of data, making manual classification of celestial objects impractical. This project focuses on the automated classification of three major types of astronomical objects:
🌌 Galaxy
🔭 Quasar (QSO)
⭐ Star
The proposed approach uses a Swin Transformer, a hierarchical Vision Transformer that applies shifted-window self-attention to capture both local and global feature relationships. To evaluate its effectiveness, the Swin Transformer is compared with a traditional CNN and a standard Vision Transformer (ViT) using the same dataset and training methodology.


🎯 Objectives
Automatically classify astronomical objects from SDSS data. Classify objects into Galaxy, QSO, and Star categories. Handle the natural class imbalance present in astronomical survey data. Apply a Swin Transformer for hierarchical feature learning. Capture both local and global feature relationships using shifted-window attention. Compare Swin Transformer performance with CNN and ViT. Evaluate models using accuracy, precision, recall, and F1-score. Reduce confusion between visually and spectrally similar astronomical classes.


🔄 System Workflow

              SDSS17 Dataset            
                   ↓                  
             Data Analysis             
                   ↓               
       Class Distribution Analysis     
                   ↓  
           Data Preprocessing
                   ↓
       Z-Score Feature Normalization
                   ↓
          80% Train / 20% Test
                   ↓
       ┌───────────┼───────────┐
       ↓           ↓           ↓
      CNN         ViT        Swin
       ↓           ↓           ↓
       └───────────┼───────────┘
                   ↓
              Model Evaluation
                   ↓
       Accuracy / Precision / Recall
                   ↓
                F1-Score
                   ↓
          Model Comparison
                   ↓
       Swin Transformer Selected

🏗️ Model Comparison
Three different architectures are evaluated:
1. CNN
A custom CNN is used as the traditional deep-learning baseline.
It consists of:
3 × 3 convolution layers
Batch normalization
ReLU activation
Max pooling
Dropout
Fully connected classification layer
The CNN provides a baseline for comparison with the Transformer architectures.

2. Vision Transformer (ViT)
The ViT baseline processes the image as a sequence of patch tokens using global self-attention.
Unlike Swin Transformer, it does not use local windowing or hierarchical spatial downsampling.

3. Swin Transformer
The proposed model uses:
Local window attention
Shifted window attention
Hierarchical representation
Patch merging
Global average pooling
Linear classification head


📊 Experimental Results
The three models were evaluated using the same 20,000-sample test set.
Overall Model Accuracy

i) CNN	76.32%   
ii) ViT	96.59%   
iii) Swin Transformer	97.25%

The Swin Transformer achieved the highest reported accuracy of 97.25%, compared with 96.59% for ViT and 76.32% for CNN.
