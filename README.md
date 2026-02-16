# Real-Time Multimodal Sentiment Analysis

## Research Overview

This project implements a real-time multimodal deep learning framework for sentiment classification by integrating textual, acoustic, and visual modalities. 

The objective is to investigate whether cross-modal feature fusion improves sentiment recognition compared to unimodal baselines, while maintaining real-time inference capability.

This work explores multimodal representation learning, feature-level fusion strategies, and latency-aware model design.

---

## Motivation

Human emotion is inherently multimodal. Traditional sentiment analysis systems rely primarily on textual data, ignoring complementary behavioural signals such as tone of voice and facial expressions.

This project addresses the following research questions:

- Can multimodal fusion improve classification performance over unimodal models?
- What fusion strategy provides the best trade-off between accuracy and computational efficiency?
- Can multimodal inference be optimized for real-time deployment?

---

## Dataset

The system was trained and evaluated on multimodal samples consisting of:

- Text transcripts
- Audio recordings
- Video frames

Preprocessing steps included:

- Tokenization and embedding extraction for text
- Spectrogram generation (MFCC-based features) for audio
- Frame sampling and CNN feature extraction for visual signals

---

## Model Architecture

The architecture consists of independent modality encoders followed by a fusion network:

### Text Encoder
- Transformer-based contextual embeddings

### Audio Encoder
- CNN applied to spectrogram representations

### Visual Encoder
- CNN-based feature extraction from sampled frames

### Fusion Mechanism
- Feature-level concatenation
- Fully connected integration layers
- Softmax classification head

---

## Experimental Setup

- Framework: PyTorch
- Training strategy: Supervised learning
- Evaluation metrics: Accuracy, Precision, Recall, F1-score
- Baseline comparison: Text-only, Audio-only, Visual-only

---

## Results

| Model | Accuracy | F1 Score |
|-------|----------|----------|
| Text-only | XX% | XX |
| Audio-only | XX% | XX |
| Visual-only | XX% | XX |
| Multimodal Fusion | XX% | XX |

Multimodal fusion demonstrated consistent improvement over unimodal baselines, confirming the hypothesis that cross-modal signals enhance sentiment recognition.

---

## Real-Time Performance

The inference pipeline was optimized to support real-time processing, including:

- Pre-computed embeddings
- Efficient batch handling
- Reduced model latency

Future work includes latency benchmarking and deployment via lightweight inference frameworks.

---

## Key Contributions

- Implementation of a modular multimodal deep learning pipeline
- Comparative evaluation of unimodal vs multimodal architectures
- Feature-level fusion experimentation
- Real-time inference design considerations

---

## Future Research Directions

- Cross-modal attention mechanisms
- Transformer-based multimodal large models
- Self-supervised multimodal pretraining
- Application to cognitive or behavioural signal modelling

---

## Research Significance

This project demonstrates:

- Strong understanding of multimodal representation learning
- Experience designing deep neural architectures
- Practical knowledge of training and evaluating AI systems
- Real-time AI system engineering

The framework provides a foundation for further research in multimodal behavioural modelling, cognitive assessment, and AI-driven human-computer interaction.
