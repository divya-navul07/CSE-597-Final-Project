# CSE-597-Final-Project-COGMEN:COntextualized GNN based Multimodal Emotion recognitioN
Paper: https://paperswithcode.com/paper/cogmen-contextualized-gnn-based-multimodal

# SOTA: COGMEN

Dataset: https://paperswithcode.com/dataset/iemocap

![image](https://github.com/user-attachments/assets/66cd9a71-ee8e-415c-a170-e834e3cfa4cf)


# Overview
This project focuses on the challenge of multimodal emotion recognition within conversations using a novel architecture that uses both Graph Neural Networks (GNN) and Transformer models. It aims to accurately predict the emotions expressed in multi-party conversations by integrating auditory, visual, and textual data.

# Dataset
The project utilizes the IEMOCAP database, which contains detailed acted multi-modal emotional expressions. More details about the dataset can be found in the above Dataset link.

# Model Architecture
![image](https://github.com/user-attachments/assets/e8abed1e-e73c-4c54-bec9-dc9edb9faf2c)

Context Extractor: Utilizes a Transformer encoder to process concatenated features from multiple modalities.

Graph Formation: Builds a directed graph to model intra and inter-speaker dependencies.

Relational Graph Convolutional Network (RGCN): Aggregates features across utterances considering different relational types.

Graph Transformer: Enhances node features by integrating multi-head attention over the graph structure.

Emotion Classifier: Classifies emotions using linear layers and a softmax function to produce probability distributions over emotions.

# Installation and Requirements
1. Clone the repository: git clone https://github.com/divya-navul07/CSE-597-Final-Project

2. Install the required libraries: pip install -r requirements.txt

# Usage
To train the model, run: python train.py --config path/to/config.json

To evaluate the model, run: python evaluate.py --checkpoint path/to/model.ckpt

# Experiments and Results: 

Extensive evaluations were conducted to validate the model's performance. The model achieved significant improvements over traditional methods.

![image](https://github.com/user-attachments/assets/667e1ca1-1087-4f84-8ddf-2c9d4439c7c5)


![image](https://github.com/user-attachments/assets/dc6cca74-06ef-4c67-99c2-3de81a5487ce)


![image](https://github.com/user-attachments/assets/76c7ca06-6a34-4f87-8e55-57e7c112ba68)

![image](https://github.com/user-attachments/assets/c78b5965-f33c-430a-a764-f9e7fc774448)

Hyperparameters and Tuning: Hyperparameter tuning was performed using Comet.ml, which helped in identifying the optimal settings for achieving the best model performance. 

The key hyperparameters include:

1. Learning Rate
2. Batch Size
3. Number of Epochs
4. Window Size for Graph Formation

The training and evaluation scripts were run on a Google Colab A100 GPU.
