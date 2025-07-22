# WellnessNexus 🚀🩸

![WellnessNexus Banner](static/img/Welllness.png)

---

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)](https://www.tensorflow.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red?logo=pytorch)](https://pytorch.org/)
[![Flask](https://img.shields.io/badge/Flask-2.x-black?logo=flask)](https://flask.palletsprojects.com/)
[![Firebase](https://img.shields.io/badge/Firebase-Auth-yellow?logo=firebase)](https://firebase.google.com/)

---

# 🌟 Project Overview

**WellnessNexus** is a next-generation web platform revolutionizing medical diagnostics through AI-powered disease detection. It focuses on early identification of **Malaria** and **Leukemia** by analyzing blood cell images, making advanced healthcare accessible to everyone.

> "Empowering health with AI-driven medical solutions."

---

## 🎯 Motivation

- Early detection saves lives.
- Many regions lack access to expert diagnostics.
- AI can bridge the gap by providing fast, reliable, and affordable analysis.

---

## 🛠️ Key Features

- 🤖 **AI-Powered Analysis**: Deep learning models for blood cell image classification
- 🦠 **Multi-Disease Detection**: Malaria & Leukemia
- 🔒 **Secure Authentication**: Firebase-based user management
- 📄 **Automated PDF Reports**: Downloadable, professional diagnostic reports
- 🌐 **Modern Web UI**: Responsive, user-friendly interface
- 📊 **Confidence Graphs**: Visualize model certainty
- 💸 **Affordable & Fast**: Instant results, low cost

---

## 🏗️ Technology Stack

| Frontend | Backend | AI/ML | Auth/DB | Reports |
|----------|---------|-------|---------|---------|
| ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white) ![JS](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black) ![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?logo=bootstrap&logoColor=white) | ![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white) | ![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white) | ![Firebase](https://img.shields.io/badge/Firebase-FFCA28?logo=firebase&logoColor=black) | ![FPDF](https://img.shields.io/badge/FPDF-003366?logo=pdf&logoColor=white) |

---

## 🖥️ System Architecture

```mermaid
graph TD;
  A[User] -->|Uploads Image| B(Frontend: Web UI)
  B -->|Sends to| C(Backend: Flask API)
  C -->|Preprocess| D1[Malaria Model (Keras)]
  C -->|Preprocess| D2[Leukemia Model (PyTorch)]
  D1 -->|Prediction| E[Result Handler]
  D2 -->|Prediction| E
  E -->|Generate| F[PDF Report]
  F -->|Download| A
  C -->|Auth| G[Firebase]
```

---

## 🧬 Model Details

### 1. **Malaria Detection Model**
- **Dataset:** iarunava/cell-images-for-detecting-malaria (Kaggle)
- **Preprocessing:**
  - Rescale, rotation, shift, shear, zoom, flip
  - Target size: 150x150 px
- **Architecture:**
  - 4 Conv2D layers (32, 64, 128, 128 filters)
  - MaxPooling after each
  - Flatten → Dense(512) → Dense(1, sigmoid)
- **Parameters:** ~5.5M (trainable)
- **Training:**
  - Batch size: 32, Epochs: 10
  - Validation accuracy: ~95.3%
- **Output:** Parasitized / Uninfected

### 2. **Leukemia Detection Model**
- **Dataset:** mohammadamireshraghi/blood-cell-cancer-all-4class (Kaggle)
- **Preprocessing:**
  - Resize to 224x224, ToTensor, Normalize (ImageNet stats)
- **Architecture:**
  - 3 Conv2d layers (32, 64, 128 filters)
  - MaxPooling after each
  - Flatten → Dense(256) → Dropout(0.5) → Dense(4)
- **Parameters:** ~25.8M (trainable)
- **Training:**
  - Batch size: 16, Epochs: 10
  - Validation accuracy: up to 96.2%
- **Output:** Benign, [Malignant] Pre-B, Pro-B, Early Pre-B

---

## 🧑‍💻 User Workflow

1. **Sign Up / Log In** (Firebase Auth)
2. **Upload Blood Cell Image**
3. **AI Model Analysis** (Malaria/Leukemia)
4. **Download PDF Report** (with results & confidence graph)

---

## 🚀 Quick Start

```bash
git clone https://github.com/yourusername/wellnessnexus.git
cd wellnessnexus
pip install -r requirements.txt
# Set up Firebase config (see below)
python app.py
```

---

## 🔐 Firebase Setup
- Create a Firebase project
- Add your Firebase config to the frontend and backend
- Enable Authentication and Realtime Database

---

## 📂 Project Structure

```
wellnessnexus/
├── static/
│   ├── css/
│   ├── js/
│   ├── img/
│   └── lib/
├── templates/
│   ├── index.html
│   ├── form.html
│   ├── about.html
│   └── ...
├── models/
│   ├── final_malaria_model.keras
│   └── leukemia_detection_cnn.pth
├── malaria_routes.py
├── leukemia_routes.py
├── app.py
└── ...
```

---

## ❓ FAQ: Project Defense Questions

### Frontend
1. What technologies did you use for the frontend?
2. How does a user interact with your platform?
3. How is user authentication handled?
4. How do you handle file uploads?
5. How do you display results and reports?

### Backend
6. What framework did you use for the backend?
7. How are your routes organized?
8. How do you preprocess images?
9. How do you load and use your AI models?
10. How do you generate PDF reports?
11. How do you ensure security and privacy?

### Models
12. What datasets did you use?
13. What preprocessing steps are applied?
14. Describe your model architectures.
15. How many parameters do your models have?
16. What are your models' validation accuracies?

---

## 🤝 Contributing

We welcome contributions! Please fork the repo, create a branch, and submit a pull request. For major changes, open an issue first to discuss what you’d like to change.

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 📞 Contact

- Email: wellnessnuxes@gmail.com
- Phone: 0317 7990549 | 03409834157
- [LinkedIn @sirihive](https://www.linkedin.com/company/sirihive/)
- 🌐 [Github @Sirihive](https://github.com/sirihive/sirihive)

---

## 🙏 Acknowledgments

- SiriHive – Our future company, InshaAllah, and the vision behind this project

- All contributors, mentors, and supporters who made this journey possible

---

Developed with ❤️ by SiriHive
