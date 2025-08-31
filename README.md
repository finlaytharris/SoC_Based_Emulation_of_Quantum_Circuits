# SoC-Based Quantum Circuit Emulator  
**Hardware-Accelerated Quantum Gates & QFT on Ultra96-V2 MPSoC**  


## General Description of the Project  

Quantum computing promises exponential speedups but physical quantum processors remain noisy, resource-limited, and expensive. Classical emulators provide accessibility, but software-only approaches lack the speed and parallelism needed to resemble real hardware.  

This project introduces a **System-on-Chip (SoC) based quantum circuit emulator** built on the **Avnet Ultra96-V2 MPSoC (Zynq UltraScale+)**. It combines FPGA parallelism with interactive Python tools for **real-time emulation of quantum gates and algorithms**.  

The design implements fundamental **single- and two-qubit gates (X, Y, Z, H, S, T, SWAP)** and a **3-qubit Quantum Fourier Transform (QFT)** in FPGA logic, with **Python + Voila dashboards** for Bloch sphere visualisation and interactive experimentation.  

This contribution demonstrates how **SoC-based emulation** bridges the gap between theoretical algorithms and practical research/education by enabling fast, open, and reusable **quantum-classical hybrid experimentation**.  

---

## Main Contributions  

-  **Quantum Gate Emulation**: X, Y, Z, H, S, T, SWAP  
-  **3-Qubit QFT Implementation** with AXI4-Lite communication  
-  **Interactive PYNQ + Voila GUI** for gate selection and visualisation  
-  **Bloch Sphere Rendering** of qubit transformations  
-  **Open & Modular HDL Design** (Model Composer + Vivado)  

---

## Hardware Prerequisites  

- **Ultra96-V2 MPSoC Board** (Zynq UltraScale+)  
- **PYNQ v3.0+** environment  
- **Vivado / Model Composer** for building hardware  
- **Jupyter Lab + Voila** for running the interactive GUI  

---

## 📂 Repository Structure  

- /notebooks — Jupyter notebooks for gate + QFT demos  
- /hardware — Model Composer + Vivado project files  
- /bitstreams — Prebuilt FPGA bitstreams for Ultra96-V2  
- /docs — Report, diagrams, and screenshots  
- README.md — This file  
- LICENSE — Open-source license  

---

## How to Build & Run  

### Quickstart (Prebuilt Bitstream)  

- Clone this repo on the Ultra96-V2  
- Load the bitstream from /bitstreams onto the PL  
- Start Jupyter Lab  
- Open notebooks:  
  - notebooks/gate_demo.ipynb → test single-qubit & two-qubit gates  
  - notebooks/qft_demo.ipynb → run a 3-qubit QFT demo  
- For GUI-only interaction (no notebook editing), launch with Voila:  
  - voila notebooks/qft_demo.ipynb  

### Build from Source  

- Open /hardware in Model Composer  
- Generate HDL and export to Vivado  
- Build the bitstream and save in /bitstreams  
- Deploy on Ultra96-V2 via PYNQ  

---

## 📊 Results  

- Pauli gates: errors ≤ 1e-10, latency ~2 ms  
- Hadamard: superpositions correct, errors up to ~45% (fixed-point limits)  
- S, T, SWAP gates: < 1e-5 error, latency 2–3 ms  
- 3-qubit QFT: ~2.8% average error, 8 ms runtime, phase errors from quantisation  
- GUI visualisation validated correctness via Bloch sphere plots  

---

## Openness & Reusability  

- Uses AXI4-Stream & AXI4-Lite interfaces → easy integration into other SoC/FPGA projects  
- Modular gate IP cores allow scaling to larger circuits  
- Designed for educational accessibility while supporting research prototyping  

---

## 🔗 Links  

- Full Report (PDF)  
- Demo Video  

---

## 📄 License  

This project is released under the MIT License.
