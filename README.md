# 🚗 Safety Monitoring Systems In Vehicles

A real-time, IoT-integrated driver safety solution that combines **drowsiness detection**, **alcohol Detection**, and **collision detection** to prevent accidents and enhance on-road safety.

## 🔍 Overview

This system monitors the driver's condition using a webcam and sensors. It includes:

- **Drowsiness Detection**: Detects if the driver is sleepy or inattentive using eye state analysis and triggers an alert.
- **Alcohol Detection**: Uses an MQ-3 alcohol sensor to monitor the driver's breath for alcohol.
- **Collision Detection**: Employs an accelerometer to detect crash-like sudden movements and can trigger alerts.

## 🎯 Key Features

- Real-time **eye tracking** using OpenCV and CNN model
- Alcohol detection using **MQ-3 sensor**
- Crash detection using an **accelerometer**
- Alerts via audio signals when danger is detected
- Modular code for easy integration with vehicle systems (e.g., GPS, GSM)
- Gsm is used to send the accurate location of accident to family members and hospitals

---

## 🧠 Drowsiness Detection System

### 👁️ Process Flow:

1. **Capture** video using webcam.
2. **Detect Face & Eyes** using Haar Cascade Classifiers.
3. **Classify Eye State** using a trained CNN (`cnnCat2.h5`).
4. **Trigger Alarm** if both eyes remain closed for a threshold duration.

### 🧱 CNN Model Architecture:

- **Conv Layers**: [32, 32, 64 filters] with 3x3 kernels
- **Dense Layers**: [128] → Output (2 classes: Open, Closed)
- **Activations**: ReLU (hidden), Softmax (output)

### 🛠️ Requirements:

```bash
pip install opencv-python
pip install tensorflow
pip install keras
pip install pygame

### 🏃 How to Run:
python drowsiness detection.py



## 🧪 Hardware Components Used

| **Feature**            | **Component**           |
|------------------------|--------------------------|
| Alcohol Detection      | MQ-3 Sensor              |
| Collision Detection    | Push Button Sensors      |
| Drowsiness Detection   | Webcam + CNN + OpenCV    |
| Alert System           | Buzzer / Speaker         |
| Mobile Notification    | GPS & GSM Modules        |







