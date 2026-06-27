# Face Cipher

A deep learning-based face verification system built using a **Siamese Neural Network**. The project performs real-time face verification using webcam images and determines whether two facial images belong to the same person.

Unlike traditional face classification, this system learns the similarity between image pairs, making it suitable for one-shot face recognition and authentication.

---

## 📌 Overview

Face Cipher uses a Siamese Neural Network trained on pairs of facial images to learn an embedding space where images of the same person are closer together than images of different people.

The model captures live images using a webcam, preprocesses them, and compares them against stored reference images for real-time identity verification.

---

## 🚀 Features

- Real-time face verification using webcam
- Siamese Neural Network architecture
- One-shot face recognition
- Custom image preprocessing pipeline
- Uses positive, negative, and anchor image pairs
- TensorFlow implementation
- LFW dataset integration for negative samples

---

## 🛠️ Tech Stack

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib

---

## 📂 Project Structure

```
├── data/
│   ├── anchor/
│   ├── positive/
│   └── negative/
├── lfw/
├── model/
├── notebooks/
│   └── Face_Cipher.ipynb
├── README.md
└── requirements.txt
```

---

## 📖 Dataset

### Positive Images
Captured using a webcam during data collection.

### Anchor Images
Reference images of the target user captured through the webcam.

### Negative Images
Collected from the **Labeled Faces in the Wild (LFW)** dataset.

---

## ⚙️ Model Architecture

The project uses a Siamese Neural Network consisting of:

- CNN-based embedding network
- Shared weights between both branches
- Distance computation between embeddings
- Binary classification for face verification

### Workflow

```
Anchor Image
        \
         \
          > Embedding Network ----\
                                  > Distance Layer --> Verification
Positive/Negative Image ---------/
```

---

## 🏋️ Training Pipeline

1. Capture anchor images
2. Capture positive images
3. Load negative images from the LFW dataset
4. Preprocess all images
5. Create positive and negative image pairs
6. Train the Siamese Neural Network
7. Save trained model

---

## 📸 Real-Time Verification

The application captures live webcam frames and compares them against stored reference images.

Verification is performed by:

- Computing image embeddings
- Measuring similarity between embeddings
- Applying a similarity threshold
- Returning Verified or Not Verified

---

## ▶️ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/face-cipher.git
cd face-cipher
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Project

Launch the notebook or Python script and execute all cells.

The pipeline performs:

- Webcam image collection
- Dataset preparation
- Model training
- Face verification
- Real-time inference

---

## 💡 Future Improvements

- Support multiple registered users
- Deploy using Streamlit or Flask
- Improve accuracy with data augmentation
- Replace custom embeddings with FaceNet or ArcFace
- Mobile and edge-device deployment
- Face recognition with liveness detection

---

## 📚 References

- TensorFlow
- OpenCV
- Labeled Faces in the Wild (LFW)
- Siamese Neural Networks for One-Shot Image Recognition

---

## 👨‍💻 Author

**Siddharth Jeedula**

B.Tech Chemical Engineering  
Indian Institute of Technology Bombay
