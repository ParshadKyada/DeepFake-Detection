# DeepFake Detection Using ResNext and LSTM

## Project Overview
This project focuses on detecting AI-generated deepfake videos using a combination of deep learning models. The system is designed to distinguish between real and manipulated videos with a high degree of accuracy, utilizing frame-level feature extraction through a ResNext Convolutional Neural Network (CNN) and temporal sequence processing using Long Short-Term Memory (LSTM) networks.

## Problem Statement
With the rapid advancement of deep learning technologies, creating realistic fake videos, known as deepfakes, has become alarmingly easy. These videos pose significant threats, including political manipulation, fake terrorism events, and personal blackmail. Detecting these deepfakes is a major challenge. This project aims to tackle this challenge by developing a deep learning-based method that can effectively identify whether a video has been manipulated or is authentic.

## Goals and Objectives
- **Detection Accuracy:** Accurately distinguish deepfake videos from real ones.
- **User Interface:** Provide a simple, user-friendly interface where users can upload a video and get a real-time prediction.
- **Real-Time Processing:** Ensure the system is capable of processing videos quickly for practical real-time applications.

## Dataset
The model was trained on a balanced dataset of real and fake videos, sourced from various public datasets:
- **FaceForensic++ (FF)**
- **Deepfake Detection Challenge (DFDC)**
- **Celeb-DF**

After preprocessing, the dataset consisted of 6,000 videos, split evenly between real and fake.

## Methodology
### 1. Data Preprocessing
- **Face Detection and Cropping:** Videos are split into frames, and faces are detected and cropped from each frame.
- **Frame Selection:** To manage computational load, only the first 150 frames of each video are used.

### 2. Model Architecture
- **ResNext CNN:** Pre-trained ResNext model (resnext50_32x4d) is used for extracting frame-level features.
- **LSTM Network:** A single LSTM layer processes the sequential frames to capture temporal features.
- **SoftMax Layer:** Provides the probability of the video being real or fake.

### 3. Training
- **Train-Test Split:** The dataset was split into 70% training and 30% testing.
- **Hyperparameters:** The model was trained using Adam optimizer with a learning rate of 0.00001 and a batch size of 4. Cross-entropy loss was used as the loss function.

## Results
The model is capable of classifying a video as real or fake with a high degree of accuracy, processing up to 10 frames per second. The confusion matrix was used to evaluate the model's performance.

## Future Work
- **Browser Plugin:** The current web-based platform can be upscaled into a browser plugin for easier access.
- **Full Body Deepfakes:** Expanding the algorithm to detect full-body deepfakes, beyond just facial manipulation.

## Acknowledgments
- Special thanks to the creators of the datasets used in this project: FaceForensic++, DFDC, and Celeb-DF.
- Thanks to the deep learning community for providing open-source tools and resources.

---

You can customize this `README.md` file according to your specific requirements or preferences. Let me know if you'd like any changes!
