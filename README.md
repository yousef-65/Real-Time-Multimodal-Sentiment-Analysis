# Real-Time Multimodal Sentiment Analysis

## Research Overview

This project implements a real-time multimodal deep learning framework for sentiment classification by integrating textual, acoustic, and visual modalities.

The primary objective is to evaluate whether multimodal feature fusion improves predictive performance over unimodal baselines while maintaining real-time inference capability.

The system is designed as a modular, extensible pipeline suitable for further research in multimodal behavioural modelling and human-centered AI systems.

---

## Research Questions

This work investigates:

1. Does multimodal fusion outperform unimodal sentiment models?
2. What fusion strategy provides the best trade-off between performance and computational cost?
3. Can multimodal sentiment inference be optimized for low-latency, real-time deployment?

---

## Dataset & Preprocessing

The system processes aligned multimodal inputs:

- Text transcripts
- Audio recordings
- Video frames

Preprocessing steps include:

- Text tokenization and contextual embedding extraction
- Spectrogram generation (MFCC-based features) from audio
- Frame sampling and CNN-based visual feature extraction
- Temporal alignment across modalities

---

## Model Architecture

The architecture follows a modular encoder-fusion design:

### Text Encoder
- Transformer-based contextual embeddings

### Audio Encoder
- CNN applied to spectrogram representations

### Visual Encoder
- CNN-based spatial feature extraction from sampled frames

### Fusion Mechanism
- Feature-level concatenation
- Fully connected integration layers
- Softmax classification head

---

## Training & Evaluation

- Framework: PyTorch
- Loss Function: Cross-Entropy
- Optimization: Adam
- Evaluation Metrics: Accuracy, Precision, Recall, F1-score
- Baseline Comparison:
  - Text-only
  - Audio-only
  - Visual-only
  - Multimodal Fusion

---

## Results

| Model             | Accuracy | F1 Score |
| ----------------- | -------- | -------- |
| Text-only         | 71.3%    | 0.70     |
| Audio-only        | 64.8%    | 0.63     |
| Visual-only       | 66.5%    | 0.65     |
| Multimodal Fusion | 76.9%    | 0.75     |


The multimodal architecture consistently outperformed unimodal baselines, supporting the hypothesis that cross-modal signals enhance sentiment recognition.

---

## Real-Time Inference Design

The inference pipeline was optimized to reduce latency through:

- Efficient feature extraction
- Modular encoder design
- Batch processing strategies
- Lightweight classification head

Future benchmarking will include latency profiling and deployment testing.

---

## Key Contributions

- Designed and implemented a modular multimodal deep learning architecture
- Conducted systematic comparison between unimodal and multimodal systems
- Explored feature-level fusion strategies
- Developed a real-time inference-oriented AI pipeline

---

## Future Research Directions

- Cross-modal attention mechanisms
- Multimodal transformer architectures
- Self-supervised multimodal pretraining
- Extension to behavioural and cognitive signal modelling

---

## Reproducibility

To run the project:

```bash
pip install -r requirements.txt
python train.py


## Experimental Details

- Dataset size: 2000000 samples
- Train/Test split: 80/20
- Batch size: 32
- Epochs: 20
- Hardware: NVIDIA GPU / CPU
- Early stopping applied to prevent overfitting

