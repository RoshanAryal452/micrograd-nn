# micrograd-nn

A lightweight, from-scratch neural network and autograd engine built in pure Python with zero external libraries.

---

## 💡 What is this project?

Normally, building modern AI requires installing massive frameworks like **PyTorch** or **TensorFlow**, which have millions of lines of complex code hidden behind the scenes.

**`micrograd-nn`** does the exact same core job, but in **just ~150 lines of simple, pure Python**. It proves that modern deep learning is not magic—just basic math and a graph of operations.

---

## ⚡ What makes it different?

This project breaks deep learning down into its two essential parts:

1. **The Math Graph Engine (`Value`)**:
   - Standard Python calculates `c = a * b` and forgets how it got there.
   - Here, `Value` remembers every operation and builds a computational tree.
   - Calling `backward()` walks backward through that tree to calculate how much each weight contributed to the error.

2. **The Neural Network (`Neuron`, `Layer`, `MLP`)**:
   - Connects simple artificial neurons into layers.
   - Takes inputs, multiplies them by weights, adds biases, and applies an activation function (`tanh`).

---

## 🔄 How It Learns (In 4 Simple Steps)

1. **Forward**: Feeds data through the network to make a prediction.
2. **Loss**: Measures how far off the prediction is from the target answer.
3. **Backward**: Backpropagates through the computational graph to calculate gradients.
4. **Step**: Nudges the weights slightly to reduce the error on the next try.

---

## 🚀 How to Run

No dependencies (no PyTorch, no NumPy) required. Run directly with Python:

```bash
python main.py
```
