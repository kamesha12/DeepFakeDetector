# 🧠 Advanced DeepFake Detection System

![DeepFake Banner](https://img.shields.io/badge/AI-Powered-blue.svg)

## 📌 Overview

DeepFakes are AI-generated synthetic media in which someone’s face or voice is convincingly replaced with someone else’s.  
Our project — **DeepFakeDetector** — combats the misuse of such technologies using an intelligent, multi-model ensemble system.

### 🔍 Features:
- Upload a face image
- Analyze it with multiple trained deep learning models
- Get individual predictions + confidence scores
- Visualize results with interactive charts
- Generate PDF and XML reports for documentation

---

## 🛠️ Tech Stack

| Component     | Technology                     |
|--------------|---------------------------------|
| Frontend UI  | Streamlit                       |
| Backend      | TensorFlow / Keras              |
| Models       | ResNet50, EfficientNetB4, InceptionV3, MobileNetV2, Xception, CustomCNN |
| Charts       | Plotly Express                  |
| Export       | FPDF (PDF), xmltodict (XML)     |
| Image Input  | PIL                             |
| Data Display | Pandas                          |

---

## 🔁 Workflow Overview

### 1. **Upload Image**
User uploads a `.jpg`, `.jpeg`, or `.png` face image using Streamlit.

### 2. **Prediction Pipeline**
- Image is saved to `uploads/`
- `predict_deepfake()` loads all models from `trained_models/`
- Each model outputs:
  - `Label`: FAKE / REAL
  - `Confidence`: Probability (0.0 to 1.0)

### 3. **Decision Engine**
- Majority voting determines the final label
- Average confidence is calculated
- Visualizations and summary are prepared

### 4. **Visualization & Reports**
- 📊 Bar, pie, and line charts
- 📝 PDF report
- 🧾 XML export
- 📥 Download buttons

---

## 🚀 How to Run the Project

### 🔧 Step 1: Clone and Setup

```bash
git clone https://github.com/kamesha12/DeepFakeDetector.git
cd deepfake-detector

# Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate      # On macOS/Linux
venv\Scripts\activate         # On Windows

# Install dependencies
pip install -r requirements.txt
#   D e e p T r u t h 
 
 
