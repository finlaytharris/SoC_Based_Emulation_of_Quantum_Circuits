Team number: AOHW25_600

Project name: SoC Based Emulation of Quantum Circuits

Link to YouTube Video(s): https://youtu.be/lxIeiJs4sNs

Link to project repository: https://github.com/finlaytharris/SoCEmulationofQuantumCircuits

University name: University of Strathclyde

Participant(s): Finlay Harris  

Email: finlay.harris.2021@uni.strath.ac.uk

Supervisor name: Dr Louise Crockett

Supervisor e-mail: louise.crockett@strath.ac.uk

Board used: Avnet Ultra96-V2 MPSoC

Software Version: Model Composer, Vivado 2023.1, PYNQ Framework

Brief description of project:
This project investigates the feasibility of using a System-on-Chip (SoC) platform for quantum circuit emulation. The Avnet Ultra96-V2 MPSoC is employed to emulate fundamental quantum gates and circuits, enabling experimentation with quantum algorithms without requiring physical quantum processors. Quantum gates including X, Y, Z, Hadamard, SWAP, S, and T have been implemented in Xilinx Model Composer and integrated into AXI-Stream IP blocks for communication between the processing system (PS) and programmable logic (PL). A 3-qubit Quantum Fourier Transform (QFT) design is implemented using AXI4-Lite for communication. PYNQ, a Python-based framework, is used to manage interactions between the PS and PL, including qubit generation, data formatting, and results visualisation. Bloch sphere plots and an interactive environment with Jupyter and Voila allow users to explore quantum gates and the QFT, enhancing accessibility for education and research. The project demonstrates that SoC-based emulation is a viable approach to quantum-classical hybrid systems.

Description of archive (explain directory structure, documents and source files):
The archive contains:
- Bitstream (.bit) files for each quantum gate and QFT implementation.
- Hardware handoff (.hwh) files for integration with PYNQ.
- Simulink (.slx) design files created in Model Composer.
- Jupyter notebooks (.ipynb) containing the PYNQ interface, Bloch sphere visualisation, and interactive controls.
- Folders containing all the required files for running each of the 3 elements in PYNQ. The 3 elements of the project include: 
			1- Quantum gates
			2- 3-Qubit Quantum Fourier Transform
			3- Both combined along with a GUI to interact with. 
- Project report and README.txt file.

Instructions to build and test project
Step 1: Open Jupyter Lab on the PYNQ environment. 
Step 2: Upload the 3 PYNQ folders onto the Ultra96-V2 board downloaded from the repo.
Step 3: Run the provided Jupyter notebooks to generate qubits, apply quantum gates, or execute the 3-qubit QFT.
Step 4: Use the Voila-based interface to visualise quantum states on Bloch spheres and interact with the emulator. Access this by visiting: http://192.168.3.1:9090/voila and then choose the folder where the quantum_Emulation.ipynb is saved.

