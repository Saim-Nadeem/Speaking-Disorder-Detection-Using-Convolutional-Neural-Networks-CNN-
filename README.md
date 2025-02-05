# **Dysarthria Detection Using Convolutional Neural Networks**

![Dysarthria Detection](/images/img1.png)

## **📌 Project Overview**
This project detects **dysarthria**, a motor speech disorder, using **Convolutional Neural Networks (CNNs)** and **audio feature extraction** techniques. The model processes speech samples and classifies them as either **normal** or **dysarthric speech** using **MFCC features** extracted with `librosa`.

---

## **📂 Dataset**
- Speech samples categorized into:
  - **Normal Speech** (`All Non Dys Wav`)
  - **Dysarthric Speech** (`All Dys Wav`)
- Each file is labeled as:
  - `0` → **Normal Speech**
  - `1` → **Dysarthric Speech**

---

## **🔍 Feature Extraction**
The following features are extracted from the speech samples using `librosa`:
- **MFCC (Mel-Frequency Cepstral Coefficients)**
- **Chroma Features**
- **Spectral Contrast**
- **Zero-Crossing Rate**
- **Tonnetz (Tonal centroid features)**

---

## **🧠 Model Architecture (1D CNN)**
The classification model is built using **1D Convolutional Neural Networks (CNNs)**:

| Layer Type       | Details                                  |
|-----------------|--------------------------------------|
| **Conv1D**      | Feature extraction from MFCCs       |
| **MaxPooling1D** | Downsampling to reduce computation |
| **Flatten**     | Converts output to 1D vector       |
| **Dense**       | Fully connected layers             |
| **Dropout**     | Prevents overfitting               |
| **Softmax**     | Outputs probability distribution   |

---

## **📈 Model Training & Evaluation**
- **Data Split**: Training & Testing using `train_test_split()`
- **Loss Function**: Categorical Crossentropy
- **Optimizer**: Adam
- **Evaluation Metric**: Accuracy


## **🚀 Future Improvements**
- Implementing **RNNs / LSTMs** for better sequential modeling
- Experimenting with **Spectrogram-based CNN architectures**
- Deploying the model using a **Flask API** for real-time predictions

---

## **📜 License**
This project is licensed under the MIT License.

---
