# Intelligent IoT Systems using ML, Edge AI, TinyML & AIoT Architectures

Welcome to the Intelligent IoT Systems repository. This project bridges the gap between Cloud AI, Edge Computing, and resource-constrained microcontrollers (TinyML). It contains end-to-end architectures, data pipelines, Machine Learning training scripts, and optimized Embedded C firmware to deploy intelligent decision-making directly onto physical hardware.

# 🚀 Overview & Architecture
Modern AIoT applications require intelligence distributed across the Edge and the Cloud. This repository demonstrates how to collect sensor data, train machine learning models using Python, optimize them for constrained hardware via TinyML, and deploy them using Embedded C.

**Key Features**

•	**Edge AI Pipelines:** Data preprocessing and feature engineering optimized for real-time streaming data.

•	**TinyML Deployment:** Quantized TensorFlow Lite Micro / Edge AI models capable of running on MCUs with <100KB of RAM.

•	**Hybrid AIoT Architecture:** Edge-to-Cloud telemetry patterns ensuring low latency and reduced bandwidth usage.


📂 Repository Structure
Plaintext

├── .github/               # CI/CD workflows for testing firmware and python scripts
├── assets/                # Architecture diagrams and performance charts
├── firmware/              # Embedded C/C++ source code for microcontrollers
│   ├── src/               # Core application logic
│   ├── include/           # Header files and exported TinyML model arrays (`model.h`)
│   └── platformio.ini     # Hardware configuration (ESP32 / STM32 / Arduino)
├── ml_pipeline/           # Python scripts for model training and quantization
│   ├── train.py           # Model training and validation script
│   ├── quantize.py        # TFLite post-training quantization (PTQ) pipeline
│   └── requirements.txt   # Python dependencies
└── README.md              # Project documentation

🛠️ Getting Started

1. Python Machine Learning Pipeline

The Python environment handles data ingestion, model exploration, training, and converting models into an explicit C-byte array for microcontrollers.

Prerequisites: Python 3.9+

# Clone the repository
git clone https://github.com/your-username/Intelligent-IoT-systems-using-Machine-Learning-Edge-AI-TinyML-and-real-world-AIoT-architectures.git
cd Intelligent-IoT-systems-using-Machine-Learning-Edge-AI-TinyML-and-real-world-AIoT-architectures/ml_pipeline

# Install dependencies
pip install -r requirements.txt

# Train the model and export the quantized TFLite model
python train.py --epochs 50
python quantize.py --input model.h5 --output ../firmware/include/model.h

2. Embedded C Firmware Deployment
The firmware directory contains the runtime engine to execute your optimized model natively on the edge hardware.

Prerequisites: PlatformIO IDE or Arduino IDE
