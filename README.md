![Platform](https://img.shields.io/badge/%F0%9F%92%BB%20Platform-Linux%20%7C%20macOS%20%7C%20Windows-informational)
[![Qiskit](https://img.shields.io/badge/Qiskit-%E2%89%A5%201.2%20-%20%236133BD?logo=Qiskit)](https://github.com/Qiskit/qiskit)

# AQC-Tensor Qiskit addon

This addon enables a Qiskit user to perform approximate quantum compilation using tensor networks,
a technique that was introduced in [arXiv:2301.08609](https://arxiv.org/abs/2301.08609).

Specifically, this package allows one to compile the _initial portion_ of a circuit into a nearly equivalent approximation of that circuit, but with much fewer layers.

It has been tested primarily on Trotter circuits to date.  It may, however, be applicable to any class of circuits where one has access to both:

1. A _great_ intermediate state, known as the "target state," that can be achieved by tensor-network simulation; and,
2. A _good_ circuit that prepares an approximation to the target state, but with fewer layers when compiled to the target hardware device.

![Compression of initial portion of circuit with AQC](docs/images/aqc-compression.png)

(Figure is taken from [arXiv:2301.08609](https://arxiv.org/abs/2301.08609).)
