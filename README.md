# Binary Classification Neural Network (PyTorch)

This repository contains a feedforward neural network implemented using **PyTorch** for binary classification tasks. It is designed to take numerical feature inputs, pass them through a hidden layer with ReLU activation, and output a binary prediction using a sigmoid function.

## 🧠 Model Architecture

```
Input Layer (input_size)
     ↓
Linear Layer (input_size → hidden_size)
     ↓
ReLU Activation
     ↓
Linear Layer (hidden_size → output_size)
     ↓
Sigmoid Activation
     ↓
Output (Binary Prediction)
```

## 📦 Dependencies

Ensure you have the following Python packages installed:

```bash
pip install torch numpy
```

## ✅ Evaluation

After training, the model is evaluated on both the training and test datasets using a threshold of `0.5` to round sigmoid outputs to binary predictions.

```python
predicted = outputs.round()
correct = (predicted == y_true.view(-1, 1)).float().sum()
accuracy = correct / y_true.size(0)
```

## 📈 Accuracy

```
Accuracy on training data: 97.80%
Accuracy on test data: 94.74%
```

## 📄 License
This project is open-source and available under the MIT License.



