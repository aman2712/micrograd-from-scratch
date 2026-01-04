# micrograd-from-scratch

This repository contains an educational implementation of a tiny automatic differentiation engine, built while following the lecture:

“The spelled-out intro to neural networks and backpropagation: building micrograd”
by Andrej Karpathy.

The goal of this project is not performance, but understanding how backpropagation and neural network training work at a fundamental level.

### What this is

- A scalar-based autograd engine
- A minimal computation graph with forward and backward passes
- Manual implementation of backpropagation using the chain rule
- Built step-by-step for learning purposes

This mirrors the ideas behind modern frameworks like PyTorch, but without tensors or optimizations.

### What I learned

- Neural networks are just mathematical expressions
- Backpropagation is systematic application of the chain rule
- Gradients represent sensitivity of the output with respect to inputs
- .backward() is not magic, it’s just graph traversal + local derivatives

### Credit & Attribution

This project is an educational reimplementation inspired by:

- Lecture: The spelled-out intro to neural networks and backpropagation
- by Andrej Karpathy
- Original micrograd repository: https://github.com/karpathy/micrograd

All core ideas belong to the original author.

### Disclaimer

This code is for learning and exploration only.
It is not intended for production use.
