# Attendance System using Face Recognition

An AI-powered attendance system that leverages face recognition technology to automatically mark attendance, minimizing manual effort and enhancing accuracy.
---

## 📌 Table of Contents
- [Abstract](#abstract)
- [Introduction](#introduction)
- [Existing System](#existing-system)
- [Proposed System](#proposed-system)
- [Implementation](#implementation)
  - Training Phase
  - Testing Phase
  - Image Augmentation
  - Face Detection
  - Face Recognition
- [Technology Stack](#technology-stack)
- [Limitations](#limitations)
- [Requirements](#requirements)

---

## 📖 Abstract
The system automates the process of marking attendance using facial recognition. This eliminates the need for manual attendance or biometric scans and offers a quick, scalable solution suitable for organizations and educational institutions.

---

## 🔍 Introduction
Traditional attendance systems are manual and time-consuming. Face recognition enables automatic attendance with minimal human effort, especially useful in large classrooms or companies.

---

## ❌ Existing System
- Manual attendance or fingerprint-based systems.
- **Drawbacks**:
  - Time-consuming (one-by-one attendance)
  - Fingerprint scanners are expensive
  - Inconvenient in large-scale environments

---

## ✅ Proposed System
- Face-recognition-based attendance using cameras.
- **Challenges**:
  - Affected by lighting conditions
  - Confusion between similar-looking faces

---

## ⚙️ Implementation

### 1. Training Phase
- Train a CNN-based model using labeled face images.
- Use image augmentation to improve dataset diversity.

### 2. Testing Phase
- Input: Group photo of people
- Steps:
  1. **Face Detection**: Using MTCNN or OpenCV
  2. **Face Extraction**
  3. **Face Embedding**: Using FaceNet
  4. **Classification**: Compare against trained embeddings

### 3. Image Augmentation
Artificially expand training data by:
- Rotating, flipping, zooming, and changing lighting of images.
- Improves model robustness and accuracy.

### 4. Face Detection
- Detect faces in images using **OpenCV** or **MTCNN**.
- Isolate faces before recognition.

### 5. Face Recognition
- Match face embeddings using CNN model (e.g., FaceNet).
- TensorFlow is used to train and infer face identity.

---

## 🧠 Convolutional Neural Networks (CNN)

- CNNs are used to classify face images by learning key facial features.
- Layers used:
  - Convolution Layer
  - ReLU Layer
  - Pooling Layer
  - Fully Connected Layer

- Converts RGB images to grayscale (Black & White) to focus on shape over color.

---

## 💻 Technology Stack
- **Languages**: Python
- **Libraries**: OpenCV, TensorFlow, Keras, MTCNN, FaceNet
- **Frameworks**: CNN-based face recognition
- **Tools**: Jupyter Notebook / Python IDE

---

## ⚠️ Limitations
- Performance drops in low-light or overexposed conditions.
- May misidentify similar-looking individuals.

---

## 🧰 Requirements
- Python 3.x
- OpenCV
- TensorFlow
- MTCNN
- FaceNet
- Numpy, Scikit-learn

Install dependencies:
```bash
pip install opencv-python tensorflow mtcnn numpy scikit-learn
