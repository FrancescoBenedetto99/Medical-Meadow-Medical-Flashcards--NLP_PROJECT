# Medical Meadow Medical Flashcards: Fine Tuning LLMs For Medical Q&A

Project for Natural Language Processing course held at @Politecnico di Milano.

## Project Overview

The primary objective of this project is to develop and refine LLM models capable of accurately answering complex medical questions. Key steps include data preprocessing, embedding and indexing of answers, and model fine-tuning and evaluation on a domain-specific dataset.

## Dataset Overview

**Medical Meadow Medical Flashcards Dataset**
The dataset used in this project contains curated medical information structured as question-answer pairs. It is tailored for building medical question-answering models and includes diverse sources and medical topics. 

For further details, you can explore the following resource:
- [Dataset Link on HuggingFace](https://huggingface.co/datasets/medalpaca/medical_meadow_medical_flashcards)
- [Paper](https://arxiv.org/pdf/2304.08247)

## Preliminary Analysis

A preliminary analysis of the dataset was performed using several techniques to gain insights into its structure:

- **Data Exploration**: Basic statistics like document length and vocabulary size.
- **Visualization**: Dimensionality reduction techniques (e.g., t-SNE) to explore the semantic distribution of documents.
- **Clustering and Topic Modeling**: Applying KMeans and LDA for topic categorization. Initial coherence and silhouette scores suggested areas for improvement in clustering quality.

## Semantic Search

The Semantic Search phase focuses on creating an efficient retrieval system for relevant medical answers based on input queries. The approach includes:

- **Answer Embedding**: Using a pre-trained Sentence Transformer model (`multi-qa-MiniLM-L6-cos-v1`) to embed answers, enabling fast similarity searches.
- **Indexing with HNSWLIB**: Leveraging HNSWLIB (Hierarchical Navigable Small World) indexing for efficient Approximate Nearest Neighbor (ANN) searches.
- **Cross-Encoder Model**: Applying a Cross-Encoder (`ms-marco-MiniLM-L-6-v2`) to re-rank the retrieved results by relevance, refining the retrieval process for contextual accuracy.

## Model Training

Model training further fine-tunes a language model for the medical question-answering task using parameter-efficient techniques:

- **Fine-Tuning with PEFT and LoRA**: Employing Parameter-Efficient Fine-Tuning (PEFT) with Low-Rank Adaptation (LoRA) for minimal-parameter fine-tuning.
- **Quantization and Optimization**: Implementing quantization to optimize model size and computational efficiency, specifically for medical Q&A tasks.
- **Evaluation**: Assessing model performance through F1 scores and QA metrics to ensure the model's answers align accurately with medical knowledge.

## Conclusions

While this project demonstrates a foundational approach to medical question-answering, the results are not yet optimal. Initial evaluations indicate that there is room for improvement.

N.B: will be modified and improved in future


---
