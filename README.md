# Face-Recognition
Face Recognition based on Raspberry Pi 5 and Webcam
# Face Recognition on Raspberry Pi (Webcam Version)

This project demonstrates a live Face Recognition system running on a Raspberry Pi using a USB Webcam. It uses OpenCV and Python to detect faces, train a model on specific individuals, and identify them in real-time.

This project is a customized implementation inspired by [Caroline Dunn's Facial Recognition project](https://github.com/carolinedunn/facial_recognition).

## Features
- **Data Collection:** Capture headshots using a USB Webcam to create a dataset.
- **Model Training:** Train a recognizer model based on the captured images.
- **Real-time Recognition:** Identify users (e.g., "Atul") via a live video feed with FPS display.

## Hardware Requirements
- Raspberry Pi 4 (or 5) recommended for better FPS.
- USB Webcam (e.g., Logitech C270 or similar).
- MicroSD Card (16GB+ recommended).
- Monitor, Keyboard, and Mouse for setup.

## Software Prerequisites
- Raspberry Pi OS (Legacy or Bullseye recommended for camera compatibility).
- Python 3
- OpenCV
- dlib
- face_recognition library

## Installation

1. **Clone the Repository**
   ```bash
   git clone [https://github.com/choudharyatul80911-beep/Face-Recognition.git]
   cd Face-Recognition
