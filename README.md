# README for Multimodal Image Retrieval System

## Overview
This project presents a **image retrieval system** that effectively retrieves images based on textual descriptions. It leverages the capabilities of **Vision Transformers (ViT)** for image encoding and **BERT** for text embedding, employing an additive attention mechanism to fuse these modalities. The system aims to enhance user experience in applications like e-commerce and multimedia search by allowing more intuitive searches through natural language.

Traditional systems often rely on visual similarity, neglecting semantic context. This work proposes a novel system that combines ViT for image encoding and BERT for text embedding, achieving improved retrieval performance as demonstrated on the FashionIQ dataset.

## Methodology
1. **Feature Extraction**
   - **Image Encoding**: Utilizes ViT to process images into feature vectors.
   - **Text Encoding**: Employs BERT to convert textual queries into embeddings.

2. **Fine-Tuning**
   - Custom architectures for ViT and BERT are fine-tuned to optimize embeddings for retrieval tasks.

3. **Multimodal Fusion**
   - Combines image and text embeddings into a unified representation using attention mechanisms.

4. **Training and Optimization**
   - The system is trained using cross-entropy loss and optimized with the AdamW optimizer.

5. **Inference**
   - Retrieves top K images based on cosine similarity between query embeddings and database images.

## Results
The system was evaluated on the FashionIQ dataset, demonstrating:
- Improved Recall, Precision, and F1 Scores as the number of retrieved images increases.
- Notable performance at higher values of K, indicating robust retrieval capabilities.

| k | Recall | Precision | F1 Score |
|---|--------|-----------|----------|
| 5 | 0.3055 | 0.1479    | 0.1994   |
| 10| 0.4342 | 0.2510    | 0.3181   |
| 20| 0.6345 | 0.4305    | 0.5130   |
| 30| 0.7314 | 0.5386    | 0.6203   |
| 50| 0.9318 | 0.7430    | 0.8268   |

## Conclusion
This study introduces an innovative approach to multimodal image retrieval that combines textual feedback with image queries, significantly improving retrieval accuracy and user experience.

## Installation
To run this project:
1. Clone the repository.
2. Install required libraries.
3. Prepare the FashionIQ dataset from Kaggle.
4. Run the training script to fine-tune the models.

For further inquiries or contributions, please contact the authors via their provided emails.

Citations:
[1] https://drive.google.com/drive/folders/1KQ5kyeSGI-lTvtb5xW2XubNO7nPyWhJw?usp=sharing
