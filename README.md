# QuantumLab

A web-based quantum computing laboratory for circuit simulation, state visualization, and algorithm exploration.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![JavaScript](https://img.shields.io/badge/javascript-ES6+-yellow.svg)
![Status](https://img.shields.io/badge/status-educational-green.svg)

## Overview

QuantumLab is an educational quantum computing simulator that runs entirely in the browser. It provides interactive tools for:

- **Circuit Builder**: Drag-and-drop interface for constructing quantum circuits
- **State Vector Simulation**: Classical simulation of quantum state evolution
- **Bloch Sphere Visualization**: Interactive 3D representation of single-qubit states
- **Algorithm Demonstrations**: Pre-built implementations of standard quantum algorithms
- **Code Export**: Generate equivalent code for Qiskit, Cirq, and Q#

## Live Demo

🔗 [View Live Demo](https://quantum-circuit-lab.netlify.app)

## Features

### Supported Gates

| Single-Qubit | Multi-Qubit | Rotation |
|--------------|-------------|----------|
| H (Hadamard) | CNOT | Rx(θ) |
| X, Y, Z (Pauli) | CZ | Ry(θ) |
| S, T (Phase) | SWAP | Rz(θ) |
| | Toffoli (CCX) | |

### Algorithm Demonstrations

- Grover's Search Algorithm
- Quantum Fourier Transform (QFT)
- VQE Ansatz Template
- QAOA Circuit Structure
- BB84 Key Distribution Protocol

## Technical Details

### Simulation Method

This simulator uses **classical state-vector simulation**, storing the full 2ⁿ-dimensional complex state vector in memory. Gate operations are implemented as matrix-vector multiplications.

### Limitations

- Browser-based JavaScript limits practical simulation to **~8-10 qubits**
- Amplitudes stored as 64-bit floating-point (IEEE 754 double precision)
- No noise modeling (planned feature)
- Educational tool, not production-grade

### What This Is NOT

- Not a substitute for real quantum hardware
- Not suitable for cryptographic applications
- Not a high-performance computing backend

## Getting Started

### Local Development

```bash
# Clone the repository
git clone https://github.com/rasidi3112/quantum-lab-circuit.git
cd quantum-lab-circuit

# Serve locally (no build step required)
npx serve .

# Open http://localhost:3000
```

### Deploy to Netlify

This is a static site with no build step required.

1. Connect your GitHub repository to Netlify
2. Set publish directory to `/` (root)
3. No build command needed

Or drag & drop the project folder to [Netlify Drop](https://app.netlify.com/drop)

## Project Structure

```
quantum-circuit-lab/
├── index.html          # Main HTML structure
├── styles.css          # CSS styling (dark theme)
├── quantum-engine.js   # Core simulation engine
├── visualizer.js       # Bloch sphere & probability charts
├── app.js              # Application logic & UI
└── README.md           # This file
```

## References

For rigorous study of quantum computing:

- Nielsen & Chuang, "Quantum Computation and Quantum Information"
- [Qiskit Textbook](https://qiskit.org/textbook)
- [IBM Quantum Learning](https://learning.quantum.ibm.com)

## License

MIT License - see [LICENSE](LICENSE) for details.

## Contributing

Contributions welcome! Please read the contributing guidelines before submitting PRs.

---

Built for educational purposes. Not affiliated with IBM, Google, or Microsoft.
