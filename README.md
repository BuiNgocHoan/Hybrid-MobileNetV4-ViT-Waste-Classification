# DS201.Q11_TrashClassification
# Lightweight Hybrid MobileNetV4-Transformer for Edge AI Waste Classification

## Project Overview
Automated waste sorting is a cornerstone of sustainable smart city management[cite: 220]. [cite_start]This project introduces a Hybrid architecture that bridges the gap between Convolutional Neural Networks (CNNs) and Vision Transformers (ViTs)[cite: 221, 222, 223]. [cite_start]By combining the speed of MobileNetV4 with the global context awareness of a Transformer bridge, we optimized the trade-off between inference speed and accuracy for deployment on edge devices.

## Dataset
- **Name:** TrashBox Dataset.
- **Size:** 17,785 images.
- **Categories:** 7 classes including Cardboard, E-waste, Glass, Medical, Metal, Paper, and Plastic.

## System Architecture & Training
- **Backbone:** MobileNet V4-Conv-Medium for efficient local feature extraction using Universal Inverted Bottleneck (UIB).
- **Transformer Bridge:** Multi-Head Self-Attention layers to capture long-range dependencies and global shapes.
- **Attention Pooling:** Aggregates token embeddings, weighting important features higher than background noise.
- **Training Strategies:** Implemented Mixup Augmentation, Cosine Annealing learning rate scheduler, and Soft Target Cross-Entropy Loss to handle class imbalance.

## Key Features & Pipeline
1. **Model Training & Benchmarking:** The Hybrid model outperforms the standard pure MobileNetV4 baseline, effectively resolving ambiguities introduced by complex waste objects.
2. **Explainable AI (XAI):** Integrated Grad-CAM to visualize activation maps, ensuring the model focuses on discriminative regions (e.g., circuits in E-waste).
3. **Live Web App:** A real-time Gradio web interface integrated with YOLOv8. The pipeline first detects waste objects using YOLOv8, followed by material classification using our Hybrid model.

## Results
- **Performance:** Achieved a Macro F1-score of 94.18%. 
- **Efficiency:** Maintained a low inference latency of 10.29 ms on a Tesla T4 GPU, achieving ~95 FPS, which is sufficient for conveyor belt systems in recycling plants.

## Acknowledgements & Contributors

**Project Authors:**
- Hoan Bui Ngoc
- Ngan Truong Kim
- Nguyen Nguyen Lam Khoi
*(Course: DS201 - Deep Learning in Data Science)*

**Academic Supervisor / Instructor:**
- **Dr. Nguyen Tan Hoang Phuoc**

*Faculty of Information Science and Engineering / Faculty of Information Systems, UIT - VNU-HCM*
