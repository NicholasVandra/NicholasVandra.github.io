---
layout: project
title: "Deep Audio Transformer Architecture"
description: "A multi-headed audio transformer designed for speech recognition, sentiment analysis, and text generation using raw audio."
img: /assets/img/projects/audio_transformer.jpg  # optional if you add one later
category: Machine Learning
tags: [deep learning, audio modeling, transformers, neural networks]
importance: 1
---

## Overview

This project introduces a **new type of audio transformer architecture** designed to process raw audio and perform multiple downstream tasks through a multi-headed decoding framework. The model combines CNNs, BiLSTMs, and Transformer layers to capture both local acoustic features and long-range temporal dependencies.

This is my primary ongoing research project as a **Data Science graduate student** and aspiring **Machine Learning Engineer**.

---

## Architecture Summary

### **1. Feature Extraction**
A hybrid **CNN + BiLSTM** extractor captures:
- Local spectral patterns (via CNN)
- Temporal dependencies (via BiLSTM)
- Combined mel-spectrogram + MFCC features

### **2. Positional Encoding**
Features are converted to sequences and embedded using sinusoidal positional encoding.

### **3. Transformer Encoder**
- Multi-head self-attention
- Feed-forward layers  
- Layer normalization + dropout  
- Trained on large mixed datasets (Common Voice, LibriTTS, MELD)

### **4. Multi-Decoder System (Novel Component)**
Each decoder specializes in a different downstream task:
- **Speech Recognition Decoder** → predicts phoneme sequences  
- **Sentiment Analysis Decoder** → predicts emotional tone  
- **Text Generation Decoder** → generates language conditioned on audio  

Finally, a **fusion decoder** merges outputs to produce a robust final inference.

---

## Goals & Contributions

- Build a fully raw-audio transformer without relying on text preprocessing.  
- Explore multi-task learning in audio systems.  
- Improve representation learning through hybrid encoders.  
- Train using memory-safe streaming pipelines for massive datasets.  
- Investigate decoder fusion as a new architecture style in audio ML.

---

## Technologies Used

- **Python, TensorFlow, PyTorch**
- **Mel Spectrograms, MFCC**
- **Transformers / Attention Mechanisms**
- **GPU Training (NVIDIA A6000)**
- **Distributed data loading (WSL, memmap)**  
- **Common Voice + LibriTTS + MELD datasets**

---

## Current Status

- **Feature extraction network fully completed** (MFCC + Mel fusion with CNN–BiLSTM pipeline)  
- **Transformer encoder fully trained, validated, and stress-tested**  
- **Speech recognition decoder built and currently undergoing evaluation**  
- **Multi-headed decoder framework implemented**  
- **Actively developing the additional decoder heads** for  
  - sentiment analysis  
  - text generation
  - classification
  - other downstream audio-based tasks  
- Preparing full evaluation metrics, cross-dataset tests, and ablation studies   

---

## Future Plans

- Implement beam search with improved phoneme handling  
- Add multilingual audio support  
- Build demo web interface for real-time speech recognition  
- Publish a paper on the multi-headed transformer architecture  

---

Just tell me which ones to include!
