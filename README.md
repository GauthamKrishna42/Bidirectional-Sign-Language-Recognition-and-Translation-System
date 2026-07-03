# Bidirectional Sign Language Recognition and Translation System

## Overview

The **Bidirectional Sign Language Recognition and Translation System** is an AI-powered application developed to bridge the communication gap between hearing individuals and the deaf or hard-of-hearing community. The system enables seamless two-way communication by translating sign language into text and converting text into corresponding sign language representations.

The project combines Computer Vision, Deep Learning, and Large Language Models to recognize hand gestures in real time, improve translation quality, and provide an accessible communication platform through an interactive web interface.

---

## Features

- Real-time sign language recognition using a webcam
- Hand landmark detection using MediaPipe
- Background subtraction with MOG2 for improved gesture detection
- CNN-based hand gesture classification
- Sentence refinement using Google's Gemini API
- Bidirectional translation:
  - Sign Language → Text
  - Text → Sign Language
- Interactive web interface built with Streamlit
- High-accuracy deep learning model for gesture recognition

---

## System Workflow

### Sign Language to Text

1. Capture live video through webcam.
2. Detect and track hand landmarks.
3. Apply preprocessing and background subtraction.
4. Classify gestures using a trained CNN model.
5. Generate predicted alphabets.
6. Refine predictions into grammatically meaningful sentences using Gemini AI.
7. Display the translated output.

### Text to Sign Language

1. Accept text input from the user.
2. Process and tokenize the input.
3. Map each character or word to its corresponding sign representation.
4. Display the generated sign sequence.

---

## Technology Stack

| Category | Technologies |
|----------|--------------|
| Programming Language | Python |
| Deep Learning | TensorFlow, Keras |
| Computer Vision | OpenCV, MediaPipe |
| AI Integration | Google Gemini API |
| Web Framework | Streamlit |
| Data Processing | NumPy, JSON |

---

## Dataset

The gesture recognition model was trained using the **ASL Alphabet Dataset** available on Kaggle.

**Dataset:** ASL Alphabet  
**Source:** https://www.kaggle.com/datasets/grassknoted/asl-alphabet/data

### Dataset Details

- 87,000 training images
- 29 classes
  - 26 English alphabets (A–Z)
  - SPACE
  - DELETE
  - NOTHING
- Image resolution: 200 × 200 pixels
- Designed for American Sign Language (ASL) gesture recognition

The dataset provides sufficient variation in hand orientations and backgrounds, making it suitable for training deep learning models for real-time sign language recognition. :contentReference[oaicite:0]{index=0}

---

## Project Structure

```text
Bidirectional-Sign-Language-Recognition-and-Translation-System/

│── app.py
│── app2.py
│── display.py
│── model_99.h5
│── index_to_class_mapping.json
│── requirements.txt
│── README.md
│
├── asl_alphabet_train/
├── asl_alphabet_test/
├── sign/
```

---

## Installation

### Clone the repository

```bash
git clone https://github.com/<your-username>/Bidirectional-Sign-Language-Recognition-and-Translation-System.git
```

### Navigate to the project directory

```bash
cd Bidirectional-Sign-Language-Recognition-and-Translation-System
```

### Create a virtual environment

```bash
python -m venv venv
```

### Activate the virtual environment

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Application

Launch the Streamlit application using:

```bash
streamlit run app.py
```

The application will automatically open in your default web browser.

---

## Model

The gesture recognition module uses a Convolutional Neural Network (CNN) trained on an American Sign Language (ASL) alphabet dataset. The trained model is stored as:

```text
model_99.h5
```

The model predicts individual hand gestures, which are subsequently refined into meaningful sentences using Google's Gemini API.

---

## Applications

- Assistive communication
- Educational institutions
- Public service accessibility
- Healthcare communication
- Smart classrooms
- Human-computer interaction research

---

## Future Enhancements

- Support for Indian Sign Language (ISL)
- Continuous sentence recognition
- Real-time speech synthesis
- Mobile application support
- Transformer-based gesture recognition models
- Multilingual translation support
- Improved robustness under varying lighting conditions

---

## License

This project was developed for academic and educational purposes. It may be used for learning, research, and non-commercial applications with appropriate attribution.
