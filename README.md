# Multi-Modal Emotion Recognition Using Facial, Text, and Speech Inputs

> **Research Project / Master's Thesis**

We're currently preparing this work for publication.  
For this reason, only the **Abstract** and **Keywords** are publicly available at this stage.

---

## Abstract

Emotion recognition is a central problem in affective computing, largely because human emotions are subtle and often expressed through multiple channels at once. Models that rely on only one modality typically struggle to capture these nuances, especially when training data is limited or inconsistent.

In this study, we propose a robust multimodal emotion recognition system that integrates **facial expressions, acoustic cues, and spoken text**. Functionally, the system accepts dynamic video sequences as input and automatically extracts synchronized visual, acoustic, and linguistic streams. Its primary objective is to synthesize these heterogeneous signals to produce a definitive discrete emotion classification — **Anger, Happy, Neutral, and Sad** — that represents the subject's affective state.

Unlike traditional static averaging, the system employs a **Gated BiGRU Temporal Fusion Network (GBTFN)** that dynamically balances modalities using Sigmoid gating and bidirectional temporal context to model emotional dynamics.

For visual recognition, we utilize a unified **EVA-02 Vision Transformer** with partial fine-tuning and Mixup regularization to retain robust generic features. For textual analysis, spoken dialogue is transcribed using **OpenAI Whisper** and processed by a fine-tuned **BERT** model to capture semantic context. Complementing this, the acoustic stream is handled by a hybrid **WavLM + CNN-BiLSTM** architecture to extract paralinguistic features such as prosody and pitch.

To address data scarcity and class imbalance, we expand existing datasets with synthetic samples generated using **Generative AI**, including **Sora** for generating realistic fearful facial expressions and **ChatGPT/Gemini** for augmenting neutral textual data.

Experimental results demonstrate robust unimodal test accuracies of **93.38% (visual)**, **96.49% (textual)**, and **88.78% (acoustic)**. Crucially, the complete **Gated BiGRU Temporal Fusion Network (GBTFN)** achieves a highly competitive **69.14% accuracy on the IEMOCAP dataset** under a rigorous **5-fold Leave-One-Session-Out (LOSO)** protocol. These results highlight the effectiveness of gated temporal modeling in resolving modality conflicts and tracking heterogeneous emotional dynamics.

---

## Keywords

`Multi-Modal Emotion Recognition` · `EVA-02` · `WavLM` · `Temporal Fusion` · `Generative AI Augmentation` · `BERT`

---

> 🔒 **Publication Status**
>
> This repository is currently restricted to the publicly shareable material from the thesis. Additional implementation details, datasets, experiments, and source code will be made available following publication.
