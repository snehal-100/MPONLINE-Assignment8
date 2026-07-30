# Handwritten Digit Recognition using Artificial Neural Networks (ANN)

**Author:** Akshat Garg  

**Registration Number:** 23BCE10641 

**Application Number:** IN26011052

**Batch Number:** 1A

**Email ID:** akshat.23bce10641@vitbhopal.ac.in  

## Objective
The objective of this project is to develop an Artificial Neural Network (ANN) using TensorFlow/Keras to classify handwritten digits (0–9) from the MNIST dataset to automate postal code recognition[cite: 2].

## Dataset Link
- [Kaggle: MNIST in CSV](https://www.kaggle.com/datasets/oddrationale/mnist-in-csv)[cite: 2]

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `tensorflow` / `keras`
- `scikit-learn`
- `kaggle`

## Methodology
1. **Data Understanding**: Analyzed $28 \times 28$ pixel feature representations (784 features) and visualized raw digit samples[cite: 2].
2. **Data Preprocessing**:
   - Verified no missing values[cite: 2].
   - Normalized pixel values to the range $[0, 1]$[cite: 2].
   - Split dataset into 80% training (48,000 samples) and 20% testing (12,000 samples)[cite: 2].
   - Applied One-Hot Encoding to the target labels[cite: 2].
3. **Model Architecture**:
   - **Input Layer**: 784 nodes[cite: 2]
   - **Hidden Layer 1**: 128 neurons (ReLU activation)[cite: 2]
   - **Hidden Layer 2**: 64 neurons (ReLU activation)[cite: 2]
   - **Output Layer**: 10 neurons (Softmax activation)[cite: 2]
4. **Model Compilation & Training**:
   - **Optimizer**: Adam[cite: 2]
   - **Loss Function**: Categorical Crossentropy[cite: 2]
   - Trained for 10 epochs[cite: 2].
5. **Evaluation**: Computed test accuracy, loss, confusion matrix, classification report, and plotted accuracy/loss curves per epoch[cite: 2].

## Model Architecture Summary

| Layer | Type | Output Shape | Param # |
| :--- | :--- | :--- | :--- |
| `dense` | Dense (ReLU) | (None, 128) | 100,480 |
| `dense_1` | Dense (ReLU) | (None, 64) | 8,256 |
| `dense_2` | Dense (Softmax) | (None, 10) | 650 |

## Results
- **Test Accuracy:** 97.41%[cite: 2]
- **Test Loss:** 0.0983[cite: 2]
- **Macro F1-Score:** 0.9739[cite: 2]

## Conclusion
The multi-layer ANN accurately classifies handwritten digits, proving the effectiveness of deep hidden layers for automatic feature extraction[cite: 2]. While fully connected networks perform well on normalized datasets like MNIST, CNN architectures remain preferable for complex computer vision tasks due to spatial translation invariance[cite: 2].