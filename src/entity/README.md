<!-- Banner / Hero Image -->
<p align="center">
  <img src="https://raw.githubusercontent.com/dhirajpawar25/Vehicle-Insurance-Project/main/assets/banner.png" alt="Vehicle Insurance Project Banner" width="100%" />
</p>

<h1 align="center">🚗 Vehicle Insurance Risk Prediction — End-to-End MLOps Project</h1>

<p align="center">
  <b>Machine Learning | MLOps | AWS | CI/CD | Docker | Flask | MongoDB | EC2 Deployment</b>
</p>

<p align="center">
  <a href="https://github.com/dhirajpawar25/Vehicle-Insurance-Project/stargazers"><img src="https://img.shields.io/github/stars/dhirajpawar25/Vehicle-Insurance-Project?style=social" /></a>
  <a href="https://github.com/dhirajpawar25/Vehicle-Insurance-Project/network/members"><img src="https://img.shields.io/github/forks/dhirajpawar25/Vehicle-Insurance-Project?style=social" /></a>
  <a href="https://github.com/dhirajpawar25/Vehicle-Insurance-Project/issues"><img src="https://img.shields.io/github/issues/dhirajpawar25/Vehicle-Insurance-Project" /></a>
  <a href="https://github.com/dhirajpawar25/Vehicle-Insurance-Project/blob/main/LICENSE"><img src="https://img.shields.io/github/license/dhirajpawar25/Vehicle-Insurance-Project" /></a>
</p>

---

## 🧠 Overview

This project demonstrates the **complete lifecycle of an MLOps system**, from data ingestion to model deployment.  
The goal is to predict **vehicle insurance claim risk** using structured customer and vehicle data — built with a **modular, scalable, and production-ready pipeline**.

---

## 🧰 Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?logo=python" />
  <img src="https://img.shields.io/badge/Flask-Framework-000000?logo=flask" />
  <img src="https://img.shields.io/badge/MongoDB-Atlas-4DB33D?logo=mongodb" />
  <img src="https://img.shields.io/badge/AWS-S3,EC2,ECR-orange?logo=amazonaws" />
  <img src="https://img.shields.io/badge/Docker-Containerization-2496ED?logo=docker" />
  <img src="https://img.shields.io/badge/GitHub-Actions-CI%2FCD-2088FF?logo=githubactions" />
  <img src="https://img.shields.io/badge/Conda-Environment-44A833?logo=anaconda" />
  <img src="https://img.shields.io/badge/ScikitLearn-ML Models-F7931E?logo=scikitlearn" />
</p>

---

## 🧩 Architecture


---

## 🧱 End-to-End Workflow

| Phase | Description |
|-------|--------------|
| **1️⃣ Project Setup** | Created project template via `template.py`, defined package structure with `setup.py` and `pyproject.toml`. |
| **2️⃣ MongoDB Atlas Setup** | Created cluster, user, and dataset. Connected using Python and stored raw data. |
| **3️⃣ Logging & Exception Handling** | Developed reusable logger and exception modules for debugging and traceability. |
| **4️⃣ Data Ingestion** | Pulled raw data from MongoDB → Converted to DataFrame → Stored locally. |
| **5️⃣ Data Validation & Transformation** | Schema validation, missing value handling, feature engineering, and transformation pipeline. |
| **6️⃣ Model Training & Evaluation** | Trained and evaluated ML models (RandomForest, XGBoost). |
| **7️⃣ AWS Integration (S3)** | Automated model storage and retrieval on AWS S3. |
| **8️⃣ Model Pusher & Prediction Pipeline** | Integrated Flask app with trained model for real-time predictions. |
| **9️⃣ CI/CD Pipeline** | GitHub Actions → Docker → AWS ECR → EC2 (self-hosted runner). |
| **🔟 Deployment** | Application live on EC2 at `http://<EC2-IP>:5080` |

---

## ☁️ AWS Infrastructure

- **IAM** — Access control  
- **S3** — Model registry  
- **ECR** — Docker image hosting  
- **EC2 (Ubuntu)** — Model deployment  
- **GitHub Actions** — CI/CD automation  

```bash
# Environment variable setup
export AWS_ACCESS_KEY_ID="XXXX"
export AWS_SECRET_ACCESS_KEY="XXXX"
export AWS_DEFAULT_REGION="us-east-1"

flowchart LR
A[MongoDB Atlas] --> B[Data Ingestion]
B --> C[Data Validation]
C --> D[Data Transformation]
D --> E[Model Training]
E --> F[Model Evaluation]
F --> G[Model Pusher (S3 Upload)]
G --> H[Prediction Pipeline (Fast Api)]

# 1️⃣ Clone repository
git clone https://github.com/dhirajpawar25/Vehicle-Insurance-Project.git
cd Vehicle-Insurance-Project

# 2️⃣ Setup environment
conda create -n vehicle python=3.10 -y
conda activate vehicle

# 3️⃣ Install dependencies
pip install -r requirements.txt

# 4️⃣ Run Flask app
python app.py


---


