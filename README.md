# Multimodal AI: Semantic Similarity with OpenAI CLIP
### 🖼️ Bridge between Computer Vision and Natural Language Processing

This project explores **Contrastive Language-Image Pre-training (CLIP)** to analyze the semantic relationship between visual data and natural language. By leveraging OpenAI's CLIP model, the system calculates cosine similarity between image and text embeddings to perform zero-shot classification and multimodal retrieval.

## 🚀 Project Overview
Traditional computer vision models are limited to a fixed set of labels. This project utilizes CLIP's dual-encoder architecture to:
1.  **Extract Multimodal Embeddings:** Generate feature vectors for both images (Vision Transformer/ResNet) and text.
2.  **Measure Semantic Similarity:** Construct a $10 \times 10$ Cosine Similarity Matrix to evaluate how well text descriptions align with visual content.
3.  **Zero-Shot Prediction:** Generate probability distributions to classify images into categories the model was never explicitly trained on.

## 🛠️ Technical Tech Stack
* **Model:** OpenAI CLIP (Contrastive Language-Image Pre-training)
* **Frameworks:** PyTorch / TensorFlow
* **Environment:** Google Colab / Python
* **Data:** COCO (Common Objects in Context) dataset & custom-curated image sets.

## 📈 Methodology
### 1. Contrastive Pre-training
The project follows the workflow of the CLIP paper: "Learning Transferable Visual Models From Natural Language Supervision." It uses a contrastive objective to maximize the cosine similarity of the $N$ correct pairs of embeddings while minimizing the similarity of the $N^2 - N$ incorrect pairs.

### 2. Similarity Matrix Generation
A core component of this project is the generation of a **Cosine Similarity Matrix**. By comparing 10 unique text prompts against 10 specific images, the matrix quantifies the "semantic distance" between the two modalities.

### 3. Probability Distribution
Probability diagrams were created using a Softmax layer over the similarity scores, providing a confidence level for zero-shot classification tasks.

## 📂 Repository Structure
* `/results`: Contains the 10x10 Cosine Similarity Matrix and Probability Diagrams.
* `/docs`: A comprehensive essay/report on CLIP architecture and contributions.
* `README.md`: Project summary and technical details.

## 🎯 Key Findings
* **Zero-Shot Generalization:** CLIP demonstrates a remarkable ability to identify objects in custom datasets without task-specific fine-tuning.
* **Feature Alignment:** The model effectively captures complex semantic relationships (e.g., identifying a "sunset" not just by color, but by the relationship between the sun and the horizon).

---
**Author:** Hrushitha Darna  
*Project focused on Multimodal AI and Zero-Shot Learning.*
