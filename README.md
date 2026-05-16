# 🧠 Handwritten Digit Recognition using MLP (MNIST)

## 📌 Project Overview
This project implements a **Multilayer Perceptron (MLP)** model to classify handwritten digits using the **MNIST dataset**.  
The goal is to evaluate how different hyperparameters (activation functions and hidden layer sizes) affect model performance.

Two experiments were conducted to compare results:
- Experiment 1: ReLU activation with 128 hidden neurons
- Experiment 2: Sigmoid activation with 256 hidden neurons

---

## 📊 Dataset
- Dataset: MNIST
- Source: torchvision.datasets.MNIST
- Classes: 10 digits (0–9)
- Image size: 28 × 28 grayscale images

### Preprocessing Steps:
- Conversion to tensor
- Normalization: mean = 0.5, std = 0.5
- Train/Test split (standard MNIST split)

---

## 🧠 Model Architecture
A simple **MLP (Multilayer Perceptron)** is used:

- Input layer: 784 neurons (28×28 flattened image)
- Hidden layer: (128 or 256 neurons depending on experiment)
- Output layer: 10 neurons (digit classes)
- Activation functions:
  - ReLU (Experiment 1)
  - Sigmoid (Experiment 2)

---

## ⚙️ Training Details
- Loss Function: CrossEntropyLoss
- Optimizer: Adam
- Learning Rate: 0.001
- Epochs: 10
- Batch Size: 64
- Device: GPU (if available)

---

## 🧪 Experiments

### 🔹 Experiment 1
- Activation: ReLU  
- Hidden Neurons: 128  

### 🔹 Experiment 2
- Activation: Sigmoid  
- Hidden Neurons: 256  

---

## 📈 Results

| Experiment     | Activation | Hidden Units | Final Test Accuracy |
|----------------|------------|--------------|---------------------|
| ReLU_128       | ReLU       | 128          | 96.88%              |
| Sigmoid_256    | Sigmoid    | 256          | 97.86%              |

### 🔍 Observations:
- Both models achieved high accuracy (>96%).
- Sigmoid with more neurons slightly outperformed ReLU in this setup.
- MLP performs well for MNIST but is limited compared to CNNs.

---

## 📊 Visualizations
The project includes:
- Training vs Testing Loss curves
- Accuracy comparison between experiments

---

## 🚀 How to Run

### 1. Install dependencies
```bash
pip install torch torchvision matplotlib
2. Run the notebook / script
python main.py

or run the Jupyter Notebook / Google Colab cells.

📁 Project Structure
MNIST-MLP-Project/
│
├── main.ipynb
├── README.md
└── data/   (auto-downloaded MNIST dataset)
