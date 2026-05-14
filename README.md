# DS201.Q11_TrashClassification
# Lightweight Hybrid MobileNetV4-Transformer for Edge AI Waste Classification

## Project Overview
[cite_start]Automated waste sorting is a cornerstone of sustainable smart city management[cite: 220]. [cite_start]This project introduces a Hybrid architecture that bridges the gap between Convolutional Neural Networks (CNNs) and Vision Transformers (ViTs)[cite: 221, 222, 223]. [cite_start]By combining the speed of MobileNetV4 with the global context awareness of a Transformer bridge, we optimized the trade-off between inference speed and accuracy for deployment on edge devices[cite: 235, 236].

## Dataset
- [cite_start]**Name:** TrashBox Dataset[cite: 263].
- [cite_start]**Size:** 17,785 images[cite: 263].
- [cite_start]**Categories:** 7 classes including Cardboard, E-waste, Glass, Medical, Metal, Paper, and Plastic[cite: 263, 357].

## System Architecture & Training
- [cite_start]**Backbone:** MobileNet V4-Conv-Medium for efficient local feature extraction using Universal Inverted Bottleneck (UIB)[cite: 250, 279, 280].
- [cite_start]**Transformer Bridge:** Multi-Head Self-Attention layers to capture long-range dependencies and global shapes[cite: 281, 282, 288].
- [cite_start]**Attention Pooling:** Aggregates token embeddings, weighting important features higher than background noise[cite: 328].
- [cite_start]**Training Strategies:** Implemented Mixup Augmentation [cite: 272][cite_start], Cosine Annealing learning rate scheduler [cite: 306][cite_start], and Soft Target Cross-Entropy Loss to handle class imbalance[cite: 274, 275].

## Key Features & Pipeline
1. [cite_start]**Model Training & Benchmarking:** The Hybrid model outperforms the standard pure MobileNetV4 baseline, effectively resolving ambiguities introduced by complex waste objects[cite: 338, 407].
2. [cite_start]**Explainable AI (XAI):** Integrated Grad-CAM to visualize activation maps, ensuring the model focuses on discriminative regions (e.g., circuits in E-waste)[cite: 354].
3. [cite_start]**Live Web App:** A real-time Gradio web interface [cite: 355] integrated with YOLOv8. The pipeline first detects waste objects using YOLOv8, followed by material classification using our Hybrid model.

## Results
- [cite_start]**Performance:** Achieved a Macro F1-score of 94.18%[cite: 339]. 
- [cite_start]**Efficiency:** Maintained a low inference latency of 10.29 ms on a Tesla T4 GPU [cite: 226][cite_start], achieving ~95 FPS, which is sufficient for conveyor belt systems in recycling plants[cite: 418].

## Acknowledgements & Contributors

**Project Authors:**
- Hoan Bui Ngoc
- Ngan Truong Kim
- Nguyen Nguyen Lam Khoi
*(Course: DS201 - Deep Learning in Data Science)*

**Academic Supervisor / Instructor:**
- **Dr. Nguyen Tan Hoang Phuoc**

*Faculty of Information Science and Engineering / Faculty of Information Systems, UIT - VNU-HCM*
