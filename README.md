# 🚗 Automated Vehicle Dent Detection and Cost Prediction

A deep learning–powered system that automates the detection of vehicle dents, classifies damage severity, estimates repair costs, and suggests nearby repair shops — all from a single uploaded image.

## 📌 Project Overview

This project aims to modernize and streamline the traditionally manual and subjective process of vehicle dent assessment and repair cost estimation. It uses computer vision and machine learning techniques to detect dents, classify their severity, estimate the associated repair cost, and recommend nearby workshops.

## 🧠 Key Features

- **Dent Detection:** Utilizes **YOLOv8** for precise real-time detection and localization of vehicle dents.
- **Severity Classification:** Employs **DenseNet-121** to categorize dents as *Minor*, *Moderate*, or *Severe*.
- **Repair Cost Estimation:** Applies a **Random Forest Regressor** to estimate repair costs based on detected damage.
- **Repair Shop Recommendation:** Integrates **Google Places API** to suggest nearby, highly-rated workshops based on user location.
- **User Interface:** Clean and interactive web UI for easy image upload and report viewing.
- **Data Handling:** Uses **MongoDB** to store user data and past reports securely.

## 🛠️ Tech Stack

- **Frontend:** HTML, CSS, JavaScript  
- **Backend:** Python (Flask)
- **Deep Learning:** YOLOv8 (Ultralytics), DenseNet-121 (PyTorch)
- **Machine Learning:** Random Forest (scikit-learn)
- **Database:** MongoDB
- **APIs:** Google Places API

## 📂 Project Structure

```

├── frontend/               # User interface components
├── backend/                # Flask backend and ML/DL model APIs
│   ├── models/             # YOLOv8, DenseNet-121, Random Forest
│   ├── preprocessing/      # Image preprocessing scripts
│   └── routes/             # API endpoints
├── data/                   # Sample images and datasets
├── utils/                  # Helper functions
├── requirements.txt        # Required Python packages
└── README.md               # Project documentation

````

## 🔍 How It Works

1. **Upload:** User uploads a vehicle image via the web interface.
2. **Detection:** YOLOv8 detects and marks dent regions with bounding boxes.
3. **Classification:** DenseNet-121 classifies the severity of each dent.
4. **Estimation:** A trained Random Forest model predicts the estimated repair cost.
5. **Suggestions:** Google Places API fetches top-rated nearby repair shops.
6. **Output:** All results are shown in the UI and optionally exportable as PDF/CSV.

## 🔧 Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/vehicle-dent-detection.git
cd vehicle-dent-detection
````

### 2. Set up a virtual environment

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Add Google Places API key

Create a `.env` file and add:

```
GOOGLE_API_KEY=your_api_key_here
```

### 5. Run the Flask app

```bash
python app.py
```

