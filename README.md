# Bearing Fault Diagnosis using CNN & Edge AI (ESP32)

This project implements a predictive maintenance system to detect bearing faults using vibration signals. It uses a Deep Learning approach with a Convolutional Neural Network (CNN) trained on the CWRU dataset and deployed on an ESP32 for real-time monitoring.

## 🚀 Project Overview
- **Dataset:** Case Western Reserve University (CWRU) Bearing Data.
- **Goal:** Classify 4 states (Normal, Ball Fault, Inner Race Fault, Outer Race Fault).
- **Architecture:** 1D-CNN (Optimized via Keras Tuner).
- **Deployment:** TensorFlow Lite Micro on ESP32.

## 🛠️ Key Features
- **Generalization:** Trained on loads 0, 1, and 2; validated/tested on load 3 to ensure the model is robust to load variations.
- **Industrial Robustness:** Data augmentation performed by adding Gaussian Noise to simulate real factory environments.
- **Optimization:** Hyperparameter tuning using Keras Tuner for best accuracy/efficiency balance.
- **Edge AI:** Model converted to `.tflite` and then to a C++ array for ESP32 deployment.

## 📊 Performance
The model shows high resilience to noise (SNR):
| SNR (dB) | Accuracy |
|----------|----------|
| 15 dB    | 98.98%   |
| 10 dB    | 89.96%   |
| 5 dB     | 41.17%   |


## 📂 Project Structure
- `/notebooks`: Python notebooks for training, data augmentation, and TFLite conversion.
- `/model`: Saved `.h5` and `.tflite` models.
- `/esp32_code`: C++ code for Arduino IDE / ESP-IDF to run the model on the microcontroller.
- `/data`: Scripts to download and preprocess CWRU data.

#

## 👤 Author
- Jawher Majed
