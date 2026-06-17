# 🖊️ Handwritten Character Recognition using CNN

A beginner-friendly deep learning mini-project built with Python and TensorFlow/Keras that recognizes handwritten digits (0–9) using a Convolutional Neural Network trained on the MNIST dataset.

---

## 📌 Project Overview

This project demonstrates how a simple CNN can be trained to classify handwritten digits with ~99% accuracy.

---

## 🎯 Objectives

- Understand how image data is loaded and preprocessed for deep learning
- Build a CNN model from scratch using Keras
- Train and evaluate the model on the MNIST dataset
- Visualize model performance using accuracy/loss graphs and a confusion matrix


---

## 📦 Dataset

**MNIST (Modified National Institute of Standards and Technology)**

| Property | Details |
|---|---|
| Source | `keras.datasets.mnist` |
| Total images | 70,000 |
| Training images | 60,000 |
| Testing images | 10,000 |
| Image size | 28 × 28 pixels |
| Color | Grayscale (1 channel) |
| Classes | 10 (digits 0 to 9) |

The dataset is automatically downloaded when you run the notebook — no manual download required.

---

## 🏗️ Model Architecture

A simple Sequential CNN with 7 layers:

```
Input (28×28×1)
    ↓
Conv2D(32 filters, 3×3, ReLU)     → Output: 26×26×32
    ↓
MaxPooling2D(2×2)                  → Output: 13×13×32
    ↓
Conv2D(64 filters, 3×3, ReLU)     → Output: 11×11×64
    ↓
MaxPooling2D(2×2)                  → Output: 5×5×64
    ↓
Flatten()                          → Output: 1600
    ↓
Dense(64, ReLU)                    → Output: 64
    ↓
Dense(10, Softmax)                 → Output: 10 (one per digit)
```

**Compiled with:**
- Optimizer: `adam`
- Loss: `sparse_categorical_crossentropy`
- Metric: `accuracy`

**Total trainable parameters: ~121,930**

---

## 📊 Results

| Metric | Value |
|---|---|
| Training Accuracy | ~99.3% |
| Test Accuracy | ~99.1% |
| Test Loss | ~0.031 |
| Epochs trained | 5 |
| Batch size | 32 |

---

## 🛠️ Requirements

Make sure you have Python 3.7+ installed, then install the required libraries:

```bash
pip install tensorflow numpy matplotlib scikit-learn jupyter
```

Or install everything at once using:

```bash
pip install -r requirements.txt
```

**requirements.txt:**
```
tensorflow>=2.10.0
numpy>=1.21.0
matplotlib>=3.5.0
scikit-learn>=1.0.0
jupyter>=1.0.0
```

---



## 📓 Notebook Sections

| Section | Description |
|---|---|
| 1. Import Libraries | Load all required Python libraries |
| 2. Load Dataset | Load MNIST from Keras and print shapes |
| 3. Data Exploration | Display sample images and labels |
| 4. Data Preprocessing | Normalize pixels and reshape for CNN |
| 5. Build CNN Model | Define and compile the model architecture |
| 6. Train Model | Train for 5 epochs with validation |
| 7. Evaluate Model | Print accuracy/loss and plot graphs |
| 8. Predictions | Predict and display results on test images |
| 9. Confusion Matrix | Visualize per-class classification performance |
| 10. Conclusion | Summary and future improvement ideas |

---

## 🖼️ Sample Output

**Training log (5 epochs):**
```
Epoch 1/5 - loss: 0.1581 - accuracy: 0.9519 - val_accuracy: 0.9826
Epoch 2/5 - loss: 0.0502 - accuracy: 0.9845 - val_accuracy: 0.9876
Epoch 3/5 - loss: 0.0352 - accuracy: 0.9893 - val_accuracy: 0.9896
Epoch 4/5 - loss: 0.0264 - accuracy: 0.9915 - val_accuracy: 0.9903
Epoch 5/5 - loss: 0.0198 - accuracy: 0.9936 - val_accuracy: 0.9908
```

---

## 🔍 Key Concepts Covered

- **CNN (Convolutional Neural Network)** — spatial feature extraction using filters
- **Conv2D** — detects edges, curves, and patterns using sliding filters
- **MaxPooling2D** — reduces image size while preserving important features
- **Flatten** — converts 2D feature maps into a 1D vector for Dense layers
- **ReLU activation** — introduces non-linearity by zeroing negative values
- **Softmax activation** — converts raw scores into class probabilities
- **Normalization** — scaling pixel values to [0, 1] for stable training
- **Confusion Matrix** — visual tool to analyze per-class performance

---

## 🚀 Future Improvements

- Add **Dropout layers** to reduce overfitting
- Train for more epochs (10–20) for marginal accuracy gains
- Test the model on **real-world handwritten digit images**
- Extend to recognize **alphabets (A–Z)** using the EMNIST dataset
- Build a simple **web app** using Flask or Streamlit for live predictions

---

## 📄 License

This project is open-source and free to use for educational purposes.
