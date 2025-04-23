# dmcca-gat-cancer-analysis

# DMCCA-GAT Cancer Analysis

This repository contains the source code and experimental workflow used for the thesis titled:  
**"Integrating Multi-omics Data via Latent Space Construction for Breast and Bladder Cancer Analysis"**

## Abstract

Cancer remains one of the most complex and heterogeneous diseases, driven by intricate interactions across genetic, epigenetic, and transcriptional landscapes. Accurately understanding and predicting tumor characteristics, such as Tumor Mutational Burden (TMB), is critical for effective diagnosis, prognosis, and personalized treatment strategies. This research aims to address inherent challenges in integrating high-dimensional, heterogeneous multi-omics datasets—including DNA methylation, gene expression, and Copy Number Alteration (CNA)—specifically for bladder and breast cancer analysis, by building a shared latent space that captures and preserves meaningful cross-omics representations. Some of these challenges include data imbalance, dimensionality, modality-specific noise, and complex non-linear biological interactions.

To overcome these obstacles, this thesis proposes constructing a shared latent space through advanced deep-learning approaches by utilizing Deep Multiset Canonical Correlation Analysis (DMCCA) and Graph Attention Networks (GATs). The shared latent space methodology provides a unified representation capturing crucial and intricate biological interactions across various omics modalities, as a result giving improved predictive accuracy for TMB classification. Attention mechanisms further refine this integration by dynamically focusing on the most relevant relational patterns within multiomics data, enhancing the model's ability to capture biological interactions between genes, pathways, and patient profiles. In addition, this study utilizes oversampling techniques—mainly the Synthetic Minority Oversampling Technique (SMOTE)—to offset data imbalance among TMB classes and menopausal status groups. As compared to baseline supervised machine learning models such as Logistic Regression (LR), Artificial Neural Network (ANN), and Tabular Transformer, the new GAT model with shared latent space training performed better by achieving an AUC of 0.76 and accuracy of 76.1\% for BRCA, whereas that of BLCA was 0.73 with an accuracy of 65.3\%, thereby establishing the usefulness of multi-omics integration through shared latent space learning.

## 🧬 Omics Data Used

- **Copy Number Alteration (CNA)**
- **DNA Methylation**
- **Gene Expression (GE)**
- **mRNA Expression**

Datasets are preprocessed and aligned sample-wise before fusion.

## 🧠 Model Architecture

1. **DMCCA**: Extracts a shared low-dimensional latent space from multi-omics views.
2. **SMOTE**: Applied in latent space to address class imbalance.
3. **Graph Attention Network (GAT)**: Trained on the latent space using biological feature graphs.
4. **Evaluation**: ROC, AUC, confusion matrix, and accuracy.
