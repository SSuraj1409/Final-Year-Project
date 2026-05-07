<h1 align="center">♻️ Smart Waste Classification & Sorting System</h1>
<p align="center"><i>An AI-powered intelligent waste management system using deep learning, computer vision, and embedded systems</i></p>

---

## 🌍 Introduction

Municipal Solid Waste (MSW) generation is increasing rapidly due to urbanization, industrialization, and population growth. According to global estimates, billions of tonnes of waste are generated annually, placing significant pressure on existing waste management systems and contributing to environmental, economic, and health-related challenges.

Traditional manual waste segregation methods are inefficient, inconsistent, and prone to contamination, reducing recycling effectiveness. To address this, this project proposes an **intelligent waste classification and sorting system** that leverages **deep learning and computer vision** to automate waste identification and improve recycling efficiency.

The system is designed to classify waste in real time using convolutional neural networks (CNNs) and deploy predictions through an embedded hardware setup, enabling automated physical sorting using an Arduino-based mechanism.

In addition to the core classification and sorting functionality, the system also includes a **web-based application for monitoring bin status and waste data insights**. This application stores classified waste information in **MongoDB** and provides visualisation of both real-time and historical bin data. It allows tracking of bin usage levels, waste distribution trends, and system activity, enabling better monitoring and analysis of the overall waste management process.

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
## 🔄 System Workflow Explanation

The diagram illustrates the end-to-end workflow of the Smart Waste Classification & Sorting System, showing how data flows between hardware components, the AI model, and the web application.

---

### 🔄 Process Flowchart for Waste Classification & Segregation

<div align="center">
<img src="https://i.imgur.com/J4iduvC.png" width="80%" alt="Waste Classification Flowchart"/>
</div>

<p align="center"></p>

---

### 🎥 OpenCV Pipeline for Real-Time Object Recognition

<div align="center">
<img src="https://i.imgur.com/q5zMLTh.png" width="80%" alt="OpenCV Pipeline"/>
</div>

<p align="center"></p>

---

### 1. 🟢 Object Detection (Arduino + Sensors)
The process begins when an object is placed on the platform.  
An Arduino microcontroller uses sensors to detect the presence of waste.  
If an object is detected, a ping signal is triggered and sent through serial communication to the AI system.

---

### 2. 🔁 Serial Communication Bridge (Forward Ping)
The ping signal is forwarded from the Arduino to the processing unit (Raspberry Pi).  
This acts as a trigger for the AI pipeline to begin classification.

---

### 3. 🧠 AI-Based Object Classification
Upon receiving the signal:
- The AI system activates the webcam  
- Multiple image frames are captured and preprocessed using OpenCV  
- Trained deep learning models perform inference  
- Ensemble model combines predictions for final classification  
- System outputs an index value corresponding to the predicted class  

---

### 4. 🔁 Serial Communication Bridge (Forward Index)
The predicted category index is sent back to the Arduino via serial communication.

---

### 5. ⚙️ Mechanical Sorting & Display (Arduino Output System)
The Arduino receives the classification result and:
- Rotates or adjusts the platform to the correct bin category  
- Measures bin fill level using sensors  
- Displays waste category and bin status on an LCD screen  

The system then resets and prepares for the next input.

---

### 6. 📡 Data Transmission to Backend
The Arduino forwards updated data (waste category, bin level, etc.) through serial communication to the Raspberry Pi acting as a gateway.

---

### 7. 🗄️ Database Storage & Dashboard Visualization
The Raspberry Pi:
- Stores data in MongoDB  
- Updates a web-based dashboard in real time  

Users can monitor:
- Bin fill levels  
- Waste distribution trends  
- System activity  

---

### 8. 🔚 Process Completion
If no valid classification is received, the system safely terminates the cycle.  
Otherwise, the process loops back and waits for the next object.

---

## 📸 Project Demonstration

---

### 🏗️ Structural Design of the Smart Bin

The following images show the structural planning and design phase of the Smart Waste Classification & Sorting System.

<div align="center">
<img src="https://i.imgur.com/ozZWVPq.png" width="80%" alt="Structural Design 1"/>
<br/><br/>
<img src="https://i.imgur.com/Lj7bOw4.png" width="80%" alt="Structural Design 2"/>
<br/><br/>
<img src="https://i.imgur.com/gol5gEl.png" width="80%" alt="Structural Design 3"/>
</div>

---

### ♻️ Final Smart Bin Build

The images below show the completed implementation of the AI-powered smart waste sorting system, including the integrated embedded hardware and automated sorting mechanism.

<div align="center">
<img src="https://i.imgur.com/1pfZqAI.png" width="80%" alt="Final Smart Bin Build 1"/>
<br/><br/>
<img src="https://i.imgur.com/7UyYY03.png" width="80%" alt="Final Smart Bin Build 2"/>
</div>

---

### 🌐 Web Dashboard & Bin Monitoring System

The web-based dashboard provides real-time monitoring and visualization of waste classification data, bin fill levels, and historical waste information stored in MongoDB.

<div align="center">
<img src="https://i.imgur.com/sOBaocR.png" width="80%" alt="Web Dashboard 1"/>
<br/><br/>
<img src="https://i.imgur.com/cTIRD8U.png" width="80%" alt="Web Dashboard 2"/>
</div>

---

### 🎥 Smart Bin Demonstration Video

The following demo video showcases the real-time operation of the Smart Waste Classification & Sorting System, including object detection, AI-based classification, automated sorting, and dashboard updates.

<div align="center">

[![Watch the Demo](https://i.imgur.com/WHi7U0s.png)](YOUR_YOUTUBE_VIDEO_LINK)

</div>

---
