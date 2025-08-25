# Emotion_Detection_from_Text

A Neural Network model that detects emotions (joy, sadness, anger, fear, love, surprise) from short text inputs.

> Week 5 Project — Neural Networks & Deep Learning

---

## 📌 Objective
Build and evaluate a neural network that classifies the emotion conveyed by a text snippet.

## 📊 Dataset
Recommended: **Kaggle – Emotions Dataset for NLP** by Praveen Govi (train/val/test `.txt` files with `text;label` format).  
After downloading, place the files as:
```
data/
├── train.txt
├── val.txt
└── test.txt
```

## ⚙️ Preprocessing
- Lowercasing & basic cleaning
- Tokenization with a capped vocabulary (e.g., 10k words)
- Sequence padding to a fixed length (e.g., 100 tokens)
- Label encoding to one-hot vectors

## 🧠 Model Architecture
```
Input → Embedding(128) → GlobalAveragePooling1D →
Dense(128, ReLU) → Dropout(0.3) → Dense(64, ReLU) → Dense(6, Softmax)
```
- Loss: `categorical_crossentropy`
- Optimizer: `adam`
- Metrics: `accuracy`

## 🧪 Evaluation
- Overall Accuracy on test set
- Class-wise Precision, Recall, F1-score
- Confusion Matrix heatmap


## 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- TensorFlow/Keras
- scikit-learn
- Matplotlib (and/or Seaborn)
- NLTK or spaCy for text utilities

