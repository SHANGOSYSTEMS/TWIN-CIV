# TWIN-CIV
TWIN-CIV — State Synchronization Protocol

TWIN-CIV is a high-performance state-synchronization protocol built by Shango Systems. It is engineered to coordinate localized physical industrial actuators with cloud-based virtual digital twin replicates under extreme latency, jitter, and network partitioning conditions.

This repository hosts the TWIN-CIV Interactive Control Console, a high-fidelity web-based dashboard used to monitor real-time telemetry, debug distributed consensus networks, simulate network failures, and test recovery convergence.

🏗️ Core Architecture

TWIN-CIV splits industrial asset management into a Dual Runtime Architecture:

Cloud Core Virtual Engine: Handles compute-intensive multiphysics modeling, finite element analysis (FEA), and long-term asset degradation calculations. Deployed on high-performance cloud clusters.

Edge-Hardened Microkernel: A bare-metal, low-latency control loop executing deterministic physical commands in under 1.8 milliseconds. Deployed directly on edge hardware controllers.

📂 Repository Structure

Below is the directory structure for the TWIN-CIV codebase:

├── index.html          # Unified Interactive Control Console (UI, Canvas Animations, Charts)
├── README.md           # Repository documentation and setup guide (This file)
├── user_manual.md      # Operator field guide and console step-by-step instructions
└── LICENSE             # MIT License


🚀 Quickstart Guide

Running the Control Console Locally

Since the interactive dashboard is built as an entirely self-contained, responsive single-page application (HTML5/CSS3/JS with Chart.js), no external compiler or web server setup is strictly required.

Clone the Repository:

git clone [https://github.com/SHANGOSYSTEMS/twin-civ.git](https://github.com/SHANGOSYSTEMS/twin-civ.git)
cd twin-civ


Open the Console:
Double-click index.html to open the interface directly in any modern web browser, or serve it using a lightweight local server:

# Python 3
python -m http.server 8000


Then navigate to http://localhost:8000.

🕹️ Interactive Features Overview

1. Consensus Node Ring (Section 03)

Visualizes a distributed node network running a deterministic Raft voting sequence.

Simulate Faults: Click on individual node modules in the canvas to isolate or fail them.

Trigger Elections: Initiate voter pulses to re-establish quorum among surviving candidates.

Jitter Control: Scale the latency slider to test how transaction times degrade under network lag.

2. Telemetry Packet Dispatch (Section 03)

Provides a real-time particle animation of data packets transitioning from edge PLCs up to cloud storage.

Test pipeline capacities under high-intensity streams by activating Saturated Core Flow.

Manually inject standard State Update frames or high-priority Emergency Stop interrupts.

3. Chaos Lab (Section 04)

Allows developers and operators to run simulation drills.

Inject network surges, sensor drift, and deep partition fractures.

Monitor self-healing response delays and recovery times in real-time via the integrated status feed and line graphs.

4. Low-Level Diagnostic Terminal (Section 06)

Includes an emulated command-line shell with interactive diagnostics shortcuts (sys-status, chaos-test, cluster-heal, export-blueprint).

🤝 Contributing

We welcome contributions to the TWIN-CIV framework! Please review our coding standards and guidelines:

Fork this repository.

Create your feature branch (git checkout -b feature/AmazingFeature).

Commit your changes (git commit -m 'Add some AmazingFeature').

Push to the branch (git push origin feature/AmazingFeature).

Open a Pull Request.

Please ensure all canvas operations are strictly performance-optimized to prevent frame drops on low-compute visualization terminals.

📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

Developed with ⚡ by SHANGŌ SYSTEMS.
