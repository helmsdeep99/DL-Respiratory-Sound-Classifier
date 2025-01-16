# Deep Learning Based Respiratory Sound Classifier
Developed as part of the Embedded Systems Workshop course

A portable system for detecting and classifying lung sounds using ESP32, a digital microphone, and a convolutional neural network (CNN). This project aims to automate lung sound classification for reliable, real-time respiratory diagnostics.
## Table of Contents

- [Introduction](#introduction)
- [System Overview](#system-overview)
  - [Hardware Setup](#hardware-setup)
  - [Software Workflow](#software-workflow)
- [Features](#features)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Results](#results)
- [Contributors](#contributors)
- [Acknowledgments](#acknowledgments)
- [References](#references)

---
## Introduction
Respiratory diseases significantly impact global health, necessitating efficient diagnostic tools. Traditional methods are often subjective and error-prone. This project introduces a cost-effective, portable system for detecting and classifying respiratory sounds like wheeze, stridor, rhonchi, and crackles.
## System Overview
### Hardware Setup
- **ESP32**: Captures and transmits audio data.
- **INMP-441 Microphone**: High-quality mono audio capture.
- **Stethoscope**: Enhanced audio localization for respiratory sounds.
### Software Workflow
1. **Audio Capture**: ESP32 records 1-second chunks of audio.
2. **Preprocessing**: Filters heart sounds and noise using advanced techniques.
3. **Feature Extraction**: Converts audio into Mel spectrograms.
4. **Classification**: CNN model classifies respiratory conditions.
## Features
- Real-time respiratory sound classification.
- High accuracy with Mel spectrogram-based CNN.
- Portable, low-power hardware design.
- Effective filtering techniques for noise and heart sound isolation.
## Setup and Installation
### Prerequisites
- ESP32 with INMP-441 microphone.
- Python 3.8+ and required libraries (`scipy`, `yodel`, `librosa`, etc.).
- Flask for server-side processing.
### Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/notrick30/DL-Respiratory-Sound-Classifier.git
	```
2. Set up the hardware as described in the Hardware Setup section.
3. Install dependencies:
    ```
    pip install -r requirements.txt
    ```
4. Run the Flask server:
	```bash
	python server.py
	```
5. Flash the ESP32 firmware to start capturing audio.
## Usage
1. Place the stethoscope on the patient's chest.
2. Start audio capture with the ESP32 device.
3. The Flask server processes the audio in real-time.
4. View the classification results in the GUI or terminal.
## Results
The system achieved reliable classification performance with metrics like accuracy, precision, recall, and F1 scores. Example results include the classification of wheeze and rhonchi sounds from real patient data.
## Acknowledgments
We are deeply grateful to our professor, Abhishek Srivastava, for his invaluable guidance, and to our teaching assistants, Ms. Santhoshini and Mr. Srikar, for their constant feedback.
## References
1. Deep Learning Based Portable Respiratory Sound Classification System, IEEE APCCAS 2023
2. [HF Lung V1 Dataset](https://gitlab.com/techsupportHF/HF_Lung_V1)