# WellnessNexus 🚀🩸  
![WellnessNexus Banner](https://github.com/hakgs1234/Wellnessnexus-Documentation/blob/main/white%20logo.png)

---

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)](https://www.tensorflow.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red?logo=pytorch)](https://pytorch.org/)
[![Flask](https://img.shields.io/badge/Flask-2.x-black?logo=flask)](https://flask.palletsprojects.com/)
[![Firebase](https://img.shields.io/badge/Firebase-Auth-yellow?logo=firebase)](https://firebase.google.com/)

---

## 🌟 Project Overview

**WellnessNexus** is an AI-powered web platform designed to revolutionize digital healthcare by providing intelligent diagnostics for **Malaria** and **Leukemia** through blood cell image analysis. Our mission is to make expert-level diagnostics accessible, affordable, and rapid—especially in under-resourced regions.

> "Empowering global health with intelligent diagnostics."

---

## 🎯 Motivation

- 🌍 Millions lack access to timely medical diagnostics.
- ⏱️ Early detection significantly improves treatment outcomes.
- 🤖 AI provides a scalable solution for fast, accurate disease screening.

---

## 🛠️ Key Features

- 🤖 **AI-Powered Detection** – Trained deep learning models for disease classification  
- 🦠 **Multi-Disease Analysis** – Supports Malaria & Leukemia diagnosis  
- 🔐 **Secure Auth System** – Firebase authentication for account protection  
- 📄 **Auto-Generated PDF Reports** – Printable diagnostics with result summaries  
- 📊 **Confidence Graphs** – Visual breakdown of prediction confidence  
- 💻 **Modern Web Interface** – Responsive UI for ease of use  
- 💸 **Affordable & Fast** – Instant output, no expert needed  

---

## 🏗️ Technology Stack

| Frontend | Backend | AI/ML | Auth/DB | Reports |
|----------|---------|-------|---------|---------|
| HTML5, CSS3, JavaScript, Bootstrap | Flask (Python) | TensorFlow, PyTorch | Firebase | FPDF |

---

## 🖥️ System Architecture

![System Architecture](https://github.com/hakgs1234/Wellnessnexus-Documentation/blob/main/system.png)
---

## 🧬 AI Model Details

### 🧪 Malaria Detection Model
| Attribute   | Value |
|-------------|-------|
| Dataset     | Kaggle – Malaria Cell Images |
| Input Size  | 150×150 px |
| Layers      | 4 Conv2D → MaxPooling → Flatten → Dense(512) → Output |
| Params      | ~5.5M |
| Training    | Batch: 32, Epochs: 10 |
| Accuracy    | ~95.3% |
| Output      | Parasitized / Uninfected |

### 🧪 Leukemia Detection Model
| Attribute   | Value |
|-------------|-------|
| Dataset     | Kaggle – Blood Cell Cancer ALL |
| Input Size  | 224×224 px |
| Layers      | 3 Conv2D → MaxPooling → Flatten → Dense(256) → Dropout(0.5) → Output |
| Params      | ~25.8M |
| Training    | Batch: 16, Epochs: 10 |
| Accuracy    | ~96.2% |
| Output      | Benign, Malignant Pre-B, Pro-B, Early Pre-B |

---

## 📊 Sample Confidence Graph (Markdown Representation)

**Malaria Detection Confidence (Example)**
```
Parasitized: ██████████████████ 94.3%
Uninfected : █░░░░░░░░░░░░░░░░ 5.7%
```

**Leukemia Detection Confidence (Example)**
```
Benign        : ██████████████ 40.1%
Pre-B         : ███████        20.8%
Pro-B         : █████          16.7%
Early Pre-B   : █████████      22.4%
```

---

## 🧑‍💻 User Workflow

1. Register / Login via Firebase
2. Upload blood cell image for analysis
3. Select disease (Malaria or Leukemia)
4. Receive prediction results with confidence graph
5. Download a PDF report of the analysis

---

## 🚀 Quick Start

```bash
git clone https://github.com/hakgs1234/Wellnessnexus-Documentation.git
cd wellnessnexus
pip install -r requirements.txt
# Add Firebase credentials (see below)
python app.py
```

---

## 🔐 Firebase Setup
- Create a project at Firebase Console
- Enable Email/Password Authentication
- Add Firebase Config to both frontend and backend
- Set up Firestore / Realtime Database if needed

---

## 📁 Project Structure

```
wellnessnexus/
├── static/
│   ├── css/
│   ├── js/
│   ├── img/
├── templates/
│   ├── index.html
│   ├── form.html
│   ├── about.html
├── models/
│   ├── final_malaria_model.keras
│   └── leukemia_detection_cnn.pth
├── malaria_routes.py
├── leukemia_routes.py
├── app.py
├── requirements.txt
└── README.md
```

---

## ❓ FAQ – Defense Questions

### Frontend
- What technologies power the UI?
- How is user interaction managed?
- How is authentication implemented?

### Backend
- Why did you choose Flask?
- How are the routes organized?
- How are uploaded images handled?

### AI Models
- What datasets were used?
- Describe the preprocessing techniques.
- What architecture does each model use?
- What are the model accuracies?

---

## 🤝 Contributing
We welcome contributions from the community. To contribute:
- Fork the repository
- Create a new branch (`git checkout -b feature-xyz`)
- Commit your changes
- Push to your branch (`git push origin feature-xyz`)
- Open a Pull Request

---

## 📜 License
This project is licensed under the MIT License.

---

## 📞 Contact
- 📧 Email: wellnessnuxes@gmail.com
- 📱 Phone: +92 317 7990549 | +92 340 9834157
- 🔗 [LinkedIn – SiriHive](https://www.linkedin.com/company/sirihive/)
- 🧠 [GitHub – SiriHive](https://github.com/sirihive/sirihive)

---

## 🙏 Acknowledgments
- SiriHive – Envisioned as our future company, InshaAllah. The inspiration and vision behind this project
- Our mentors, supporters, and open-source communities who guided and empowered us
- Special thanks to the medical AI community and data contributors

---

Developed with ❤️ by Team SiriHive
