<h1 align="center">♻️ Smart Waste Classification & Sorting System</h1>
<p align="center"><i>An AI-powered intelligent waste management system using deep learning, computer vision, and embedded systems</i></p>

---

## 🌍 Introduction

Municipal Solid Waste (MSW) generation is increasing rapidly due to urbanization, industrialization, and population growth. According to global estimates, billions of tonnes of waste are generated annually, placing significant pressure on existing waste management systems and contributing to environmental, economic, and health-related challenges.

Traditional manual waste segregation methods are inefficient, inconsistent, and prone to contamination, reducing recycling effectiveness. To address this, this project proposes an **intelligent waste classification and sorting system** that leverages **deep learning and computer vision** to automate waste identification and improve recycling efficiency.

The system is designed to classify waste in real time using convolutional neural networks (CNNs) and deploy predictions through an embedded hardware setup, enabling automated physical sorting using an Arduino-based mechanism.

---

## 🤖 System Overview

The system performs real-time waste classification through the following pipeline:

1. Webcam captures live input stream  
2. OpenCV processes and preprocesses image frames  
3. Deep learning models perform inference  
4. Ensemble strategy combines predictions from multiple models  
5. Final prediction is sent to Arduino via serial communication  
6. Arduino triggers mechanical sorting system  

---

## 🧠 Model Architecture

The system uses multiple convolutional neural network models:

- EfficientNet-B0 (Pretrained)
- ResNet-50 (Pretrained)
- MobileNetV3-Large (Pretrained)
- Custom CNN (Baseline comparison)

To improve performance and robustness, an **ensemble learning approach** is used to combine predictions from pretrained models, reducing individual model errors and improving stability in real-world conditions.

All pretrained models are converted into **ONNX format** and deployed on an edge device (Raspberry Pi) for real-time inference.

---

## 👥 Team Members

- Suraj Srinivasan  
- Av Madrigalejos  
- Chris Martin Edappady  

---

## 🙋‍♂️ My Contribution – Suraj Srinivasan

I was responsible for the **deep learning system development and real-time inference pipeline**, including:

- Designing and training multiple CNN architectures  
- Implementing transfer learning using pretrained models  
- Developing the **ensemble learning strategy**  
- Converting models into **ONNX format for deployment**  
- Building the **OpenCV-based real-time classification system**  
- Integrating AI output with Arduino via serial communication  
- Testing system performance under real-world conditions  

---

## 🛠️ Technologies Used

- Python  
- PyTorch  
- OpenCV  
- Scikit-learn  
- ONNX / ONNX Runtime  
- Arduino  
- Raspberry Pi  
- Computer Vision  
- Deep Learning (CNNs)  

---
