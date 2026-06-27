#  Word for Thought – Speech Emotion Recognition using Deep CNN

## Overview

**Word for Thought** is a Speech Emotion Recognition (SER) project that classifies human speech into one of six emotions using deep learning. The model extracts meaningful acoustic features from speech recordings using **Librosa** and classifies emotions using a lightweight **3-block Convolutional Neural Network (CNN)** built with TensorFlow/Keras.

The project combines two benchmark speech emotion datasets, **RAVDESS** and **CREMA-D**, containing over **9,500** speech recordings.

---

## Objective

To classify human speech into the following six emotion categories:

*  Angry
*  Disgust
*  Fear
*  Happy
*  Neutral
*  Sad

---

## Dataset

### RAVDESS

* Professional emotional speech recordings
* 24 actors
* Speech-only samples used

### CREMA-D

* Crowd-sourced emotional speech dataset
* 91 actors
* Multiple emotional expressions

### Combined Dataset

* **Total Samples:** 9,554
* **Emotion Classes:** 6

---

## Technologies Used

* Python
* TensorFlow / Keras
* Librosa
* NumPy
* Pandas
* Matplotlib
* Scikit-learn

---

## Project Workflow

```text
Speech Audio (.wav)
        │
        ▼
Audio Preprocessing
        │
        ▼
Feature Extraction using Librosa
(Mel Spectrogram + MFCC + ZCR + RMS)
        │
        ▼
143 × 130 Feature Representation
        │
        ▼
3-Block Deep CNN
        │
        ▼
Emotion Prediction
```

---

## Feature Extraction

For every speech recording, the following acoustic features are extracted:

* Mel Spectrogram
* Mel Frequency Cepstral Coefficients (MFCC)
* Zero Crossing Rate (ZCR)
* Root Mean Square Energy (RMS)

The extracted features are combined into a unified **143 × 130** feature representation before being fed to the CNN.

---

## CNN Architecture

The model consists of:

* 3 Convolutional Blocks
* Batch Normalization
* Max Pooling
* Global Average Pooling
* Dropout Regularization
* Softmax Output Layer

---

## Model Performance

**Validation Accuracy:** **64.03%**

### Classification Performance

| Emotion | F1-Score |
| ------- | -------: |
| Angry   |     0.78 |
| Disgust |     0.57 |
| Fear    |     0.58 |
| Happy   |     0.62 |
| Neutral |     0.62 |
| Sad     |     0.60 |

---

