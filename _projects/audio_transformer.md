---
layout: page
title: Audio Transformer Research
description: Development of a multi-headed audio transformer for speech recognition, sentiment analysis, and text generation.
img: /assets/img/profile.jpg
importance: 1
category: Machine Learning
---

# Audio Transformer Research

This is my ongoing capstone and research project: designing and implementing a **next-generation audio transformer** capable of performing multiple tasks using raw or minimally processed audio.

## Goal
To create a transformer architecture that handles **speech recognition**, **sentiment analysis**, and **text generation**, each through its own decoder, and then merges the outputs into a unified representation.

## Architecture
- **Hybrid CNN–BiLSTM Feature Extractor**  
  - Mel spectrogram + MFCC input  
  - Temporal + spectral fusion  
- **Transformer Encoder**  
  - Multi-head attention  
  - Positional encoding  
  - 6 to 12 encoder layers  
- **Multiple Decoders**  
  1. Speech Recognition Decoder (phoneme prediction)  
  2. Sentiment Decoder  
  3. Language Modeling Decoder  
- **Final Multi-Headed Decoder**  
  - Concatenates the individual decoder outputs  
  - Produces a unified final prediction  

## Training Pipeline
- Custom streaming dataset generators  
- 560k+ samples across **Common Voice**, **MELD**, **LibriTTS**  
- GPU-optimized training on NVIDIA A6000  
- Chunked `.npy` storage for memory safety  
- Label smoothing + beam search decoding  

## Status
- Encoder fully trained  
- Speech recognition decoder operational  
- Multiheaded decoder in active development  

## Tools & Technologies
Python, TensorFlow/Keras, PyTorch (planned), NumPy, Matplotlib, Librosa, CUDA, Jupyter, Git, WSL2
