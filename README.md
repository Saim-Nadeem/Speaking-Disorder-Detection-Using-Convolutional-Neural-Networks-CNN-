🧠 Dysarthria Detection Using Convolutional Neural Networks (CNN)

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/Framework-TensorFlow-orange.svg)](https://www.tensorflow.org/)
[![Librosa](https://img.shields.io/badge/Audio%20Processing-Librosa-yellow.svg)](https://librosa.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> A deep learning-based system for detecting dysarthria (motor speech disorder) from audio recordings using MFCC features and 1D CNNs.

---

## 📌 Overview
This project uses **Convolutional Neural Networks** (CNNs) to identify **dysarthria**, a speech impairment, from `.wav` audio samples.  
It extracts audio features using **Librosa** and classifies speech as **normal** or **dysarthric** using a supervised learning model.

---

## 📂 Folder Structure

```
├── All Dys Wav/             # 🧑‍⚕️ Dysarthric speech samples (training)
├── All Non Dys Wav/         # 🙂 Normal speech samples (training)
├── Testing Dataset/         # 🧪 Testing speech samples
├── images/
│   └── img1.png             # 🖼️ Model diagram or visual
├── Dysarthria_Detection.ipynb   # 🧠 Jupyter notebook for full training and prediction
├── README.md                # 📘 This documentation file
```

---

## 🔍 Feature Extraction

Features are extracted from `.wav` files using the `librosa` library:
- 🎙️ MFCC (Mel Frequency Cepstral Coefficients)
- 🎵 Chroma
- 📊 Spectral Contrast
- ✂️ Zero-Crossing Rate
- 🧠 Tonnetz

---

## 🧠 CNN Model Architecture

| Layer           | Description                             |
|----------------|-----------------------------------------|
| Conv1D         | Extracts temporal patterns from MFCCs   |
| MaxPooling1D   | Downsamples feature maps                |
| Flatten        | Converts output into a dense vector     |
| Dense          | Fully connected layer                   |
| Dropout        | Prevents overfitting                    |
| Softmax        | Outputs probabilities for 2 classes     |

---

## 🧪 Sample Prediction Output

```
Input File: patient_042.wav
Prediction: Dysarthric Speech (Class 1)
Confidence: 91.7%
```

---

## ▶️ How to Run

1️⃣ **Clone the Repository**
```bash
git clone https://github.com/Saim-Nadeem/Dysarthria-Detection-CNN.git
cd Dysarthria-Detection-CNN
```

2️⃣ **Install Dependencies**
```bash
pip install -r requirements.txt
```

3️⃣ **Launch Notebook**
```bash
jupyter notebook Dysarthria_Detection.ipynb
```

4️⃣ **Upload and Predict**
- Use the testing cell to classify new `.wav` files from the `Testing Dataset/` folder.

---

## 🛠 Technologies Used

- 🐍 Python 3.9+
- 🧠 TensorFlow / Keras
- 🎧 Librosa
- 📊 NumPy, Pandas
- 📉 Scikit-learn (for train/test split, evaluation)

---

## 🔮 Future Work

- 🌀 Add LSTM/RNN for sequential modeling
- 🖼 Convert MFCC to spectrograms for 2D CNN
- 🌐 Deploy as web service using Flask or Streamlit

---

## 🖼 Image

![Model Overview](images/img1.png)

---

## 📜 License

This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for more details.

---

## 👤 Author

**Saim Nadeem**  
🔗 GitHub: [Saim-Nadeem](https://github.com/Saim-Nadeem)
