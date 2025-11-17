---
layout: project
title: "Audio Sentiment Analysis Model"
description: "A hybrid deep learning neural network that predicts sentiment directly from speech audio using MFCC–Mel fusion, CNNs, and BiLSTMs."
img: /assets/img/profile.jpg
importance: 2
category: Machine Learning
tags: [deep learning, sentiment analysis, audio, neural networks]
---

# Audio Sentiment Analysis

This project focuses on detecting **sentiment directly from raw speech audio**, not text transcripts.  
The goal is to capture emotional cues such as tone, pitch, energy, and cadence — aspects that traditional text-only models cannot detect.

---

## Motivation

Written text removes essential emotional information present in the human voice.  
To address this gap, I built a model that performs **emotion and sentiment classification from audio alone**, enabling:

- More expressive conversational AI  
- Enhanced customer-service classification  
- Emotion-aware agents and assistants  
- Better human-AI interaction  

This research later became part of a **GPT Agent** that performs real-time audio sentiment analysis.

---

## Model Architecture

### **Feature Inputs**
- **MFCCs** – capture vocal tract characteristics and emotional tone  
- **Mel Spectrograms** – capture frequency-energy distribution  

These are fused to form a rich representation of the input audio.

### **Neural Network Pipeline**
- **CNN layers** to detect local temporal–frequency features  
- **BiLSTM layers** for long-range temporal understanding  
- **Fully-connected classification head**  
- Output: **3–7 sentiment/emotion classes** (depending on dataset)

---

## Datasets

- **MELD** (Multimodal EmotionLines Dataset)  
- Custom curated speech samples  

Both are preprocessed into MFCC + Mel fusion inputs.

---

## Project Status

- Neural network is fully trained and operational  
- Integrated into an **OpenAI GPT Agent** for real-time inference  
- Evaluated on multiple emotional classes  
- Currently exploring cross-dataset generalization

---

## Future Work
- Add self-supervised pretraining for better representation learning  
- Combine with transformer-based audio encoders  
- Expand emotion categories  
- Deploy as a cloud microservice  
