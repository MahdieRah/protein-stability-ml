# 🧬 Protein Stability Prediction with ESM-2 + MLP

## Overview
This project demonstrates how to use a pretrained protein language model (ESM-2 by Meta AI) with a simple neural network to predict protein stability from sequence data.

We use:
- **ESM-2** embeddings to represent sequences
- A **PyTorch MLP model** to learn from these embeddings
- A sample dataset (replaceable with real data like ProTherm)

---

## 📁 Project Structure
```
protein-stability-prediction/
├── data/
│   └── example_data.csv           # Sample dataset (sequence + stability)
├── esm2_utils.py                  # ESM feature extractor
├── model.py                       # MLP model code (PyTorch)
├── train.py                       # Training & evaluation code
├── predict.py                     # For predicting new sequences
├── README.md                      # Project overview
├── requirements.txt               # Dependencies
└── notebook.ipynb                 # All-in-one Colab-ready version
```

---

## 🚀 How to Run (in Google Colab)
1. Open the file `notebook.ipynb`
2. Run all the cells step-by-step
3. See the training loss and test performance
4. Try predicting on your own sequences

---

## 🔍 Sample Dataset Format
```
sequence,stability_score
MVKVYAPASSANMSVGFDVL,0.85
GLSDGEWQLVLNVWGK,0.75
```

You can replace this with a dataset from [ProTherm](https://www.abren.net/protherm/) or other protein stability databases.

---

## 🧠 Model Details
- **Input**: ESM-2 embedding (1280-dimensional)
- **Model**: 3-layer MLP with ReLU, Dropout
- **Output**: Single float prediction (stability score)

---

## 📦 Dependencies
Install with:
```bash
pip install fair-esm torch pandas scikit-learn
```

---

## 📈 Future Work
- Use full ProTherm dataset for better training
- Fine-tune ESM embeddings
- Add attention-based prediction model
- Visualize embeddings with t-SNE or PCA

---

## 🤖 Credit
- Model: [Meta AI ESM-2](https://github.com/facebookresearch/esm)
- Author: *Your Name Here*
- License: MIT

---

## 🌐 How to Contribute
Fork the repo, submit pull requests, and share your improvements!
