# Urdu Image Caption Generation

This repository contains the implementation of a Transformer-based model for Urdu Image Caption Generation, presented in the study *"A Transformer-based Urdu Image Caption Generation."* The project aims to generate syntactically, contextually, and semantically correct captions in Urdu for given images. It addresses the challenges of working with low-resource languages like Urdu by leveraging state-of-the-art deep learning architectures.

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Dataset](#dataset)
- [Proposed Models](#proposed-models)
  - [CNN + Attention LSTM](#cnn--attention-lstm)
  - [CNN + Transformer](#cnn--transformer)
  - [ViT + Roberta](#vit--roberta)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Image caption generation is a bridge between Natural Language Processing (NLP) and Computer Vision (CV), designed to describe images with textual captions. While most research focuses on resource-rich languages like English, this project emphasizes Urdu, a low-resource language.

The study proposes three Seq2Seq-based architectures for Urdu caption generation:
1. **CNN + Attention LSTM** with Word2Vec embeddings.
2. **CNN + Transformer** encoder-decoder.
3. **Vision Transformer (ViT) + Roberta** encoder-decoder.

---

## Key Features

- Custom Urdu-translated subset of the Flickr8k dataset.
- Comparison of three deep learning models.
- Achieves state-of-the-art performance with BLEU and BERT-F1 scores.
- Demonstrates the effectiveness of pretraining and transformer-based approaches for low-resource languages.

---

## Dataset

### Flickr8k Urdu Subset
- **Total Images:** 1800
- **Total Captions:** 9000 Urdu captions
- **Format:** Each image is paired with 5 Urdu captions.
- **Preprocessing:** Includes punctuation removal, sentence splitting, and tokenization.

### Methodology:
<img width="315" alt="Screenshot 2025-01-19 at 8 37 22 AM" src="https://github.com/user-attachments/assets/cb0df784-86c6-45bb-bb2b-ec487900ae6a" />

---

## Proposed Models

### CNN + Attention LSTM
- Incorporates a ResNet50-based encoder for feature extraction.
- Decoder uses LSTM with a soft attention mechanism.
- Pretrained Word2Vec embeddings trained on Urdu text.

---

### CNN + Transformer
- Employs InceptionV3 as the encoder and a Transformer-based decoder.
- Enhanced performance with self-attention mechanisms in the Transformer.
<img width="708" alt="Screenshot 2025-01-19 at 8 44 16 AM" src="https://github.com/user-attachments/assets/1a0e4894-a52c-47a2-84b5-b858c8cf168c" />

---

### Vision Transformer (ViT) + Roberta
- Uses Vision Transformer (ViT) for image encoding.
- Roberta (trained on Urdu text) serves as the decoder.
- Achieves the highest scores among the models.

<img width="824" alt="Screenshot 2025-01-19 at 8 45 16 AM" src="https://github.com/user-attachments/assets/9eea9c52-2fc4-4613-8264-cb8265e09a33" />

---
## Results

The models were evaluated using BLEU, BERT-F1, and LASER metrics. The Vision Transformer + Roberta model outperformed all others.

| Model                  | BLEU-1 | BLEU-4 | BERT-F1 |
|------------------------|--------|--------|---------|
| CNN + Attention LSTM  | 71.8   | 29.1   | 81.9    |
| CNN + Transformer     | 78.9   | 37.6   | 87.0    |
| ViT + Roberta         | 86.0   | 59.0   | 90.6    |

Placeholder for **Comparison Plot**.

<img width="720" alt="Screenshot 2025-01-19 at 8 32 52 AM" src="https://github.com/user-attachments/assets/6d72c4c9-ce2a-46db-a9d1-45e6dd864f56" />
<img width="621" alt="Screenshot 2025-01-19 at 8 37 04 AM" src="https://github.com/user-attachments/assets/f7a68f16-b608-4d9a-9442-1f8ab64fe3da" />
Screenshot 2025-01-19 at 8.36.55 AM
---

<img width="577" alt="Screenshot 2025-01-19 at 8 36 40 AM" src="https://github.com/user-attachments/assets/6746afc6-176a-4113-833c-1d2967703c67" />
<img width="660" alt="Screenshot 2025-01-19 at 8 34 07 AM" src="https://github.com/user-attachments/assets/17bd5ccd-a03f-4421-a8eb-ba0feaf2aaf9" />


## Contributing

Contributions are welcome! Please open an issue or submit a pull request to improve the project.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

### References
- "A Transformer-based Urdu Image Caption Generation," Springer Nature.
- Additional references and datasets are mentioned in the [paper]([https://link-to-paper](https://link.springer.com/article/10.1007/s12652-024-04824-9)).

---

### Acknowledgments
Special thanks to the authors and contributors of the research paper for their groundbreaking work in advancing Urdu NLP and CV tasks.
