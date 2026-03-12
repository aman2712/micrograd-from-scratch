# micrograd-from-scratch

An educational implementation of a scalar-based automatic differentiation engine built from first principles to deeply understand backpropagation and neural network training.

This project reconstructs the core mechanics behind modern deep learning frameworks by implementing:

* A dynamic computation graph
* Forward propagation
* Manual backpropagation using the chain rule
* Gradient accumulation across graph nodes
* Parameter updates via gradient descent

Unlike framework-level abstractions, this implementation exposes every intermediate step of gradient computation.

---

## Architecture Overview

The engine is built around:

* A `Value` class representing scalar nodes in a computation graph
* Operator overloading to dynamically construct the graph during forward execution
* Explicit storage of parent nodes and local gradient functions
* A topologically sorted backward pass for correct gradient propagation

Backpropagation is implemented as:

1. Build the computation graph during the forward pass
2. Perform reverse topological traversal of the graph
3. Apply local derivatives using the chain rule
4. Accumulate gradients at each node

This mirrors the conceptual foundation of PyTorch’s autograd engine, but implemented at scalar granularity for clarity and educational depth.

---

## Key Learnings

* Neural networks reduce to composable mathematical expressions
* Backpropagation is structured graph traversal, not "magic"
* Gradients represent sensitivity propagation through dependencies
* Correct backward implementation requires topological ordering
* Automatic differentiation is fundamentally a graph problem

---

## Why This Project Matters

Rebuilding autograd from scratch develops:

* Deep understanding of gradient-based optimization
* Strong intuition for computational graphs
* Algorithmic thinking about dependency structures
* Systems-level understanding of ML frameworks

This project prioritizes conceptual correctness and clarity over performance.

---

## Attribution

This implementation was developed while studying:

**“The spelled-out intro to neural networks and backpropagation”**
by Andrej Karpathy

Original reference: [https://github.com/karpathy/micrograd](https://github.com/karpathy/micrograd)

All foundational ideas belong to the original author. This is an independent educational reimplementation for learning purposes.

---

## Disclaimer

This code is intended for educational exploration only and is not optimized for production use.
