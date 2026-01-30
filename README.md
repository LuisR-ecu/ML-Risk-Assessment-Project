# ML Risk Assessment Project – Churn Analytics & Deployment Demo

This project is an end-to-end **customer churn risk assessment solution** designed to mirror the type of
customer-facing, explainable, and production-aware systems built by SAS Solutions Factory teams.

It demonstrates how analytics, machine learning, modern web development, and real deployment
infrastructure can come together to deliver actionable business insights through a clean interactive dashboard.

---

## 🔍 What This Demo Does

- Visualizes customer churn risk metrics and segment-level insights  
- Allows interactive churn prediction for individual customers  
- Provides transparent model explanations for trust and interpretability  
- Mimics real-world solution architecture used in enterprise analytics teams  
- Is fully deployed as a self-hosted app running in a homelab environment  

---

## 🧠 Machine Learning Component

The predictive engine uses an interpretable **logistic regression churn risk model** built with scikit-learn.

The model generates:

- A churn probability score  
- A binary churn prediction  
- Feature-weight explanations to support decision-making  

The focus is not maximum accuracy, but **interpretability**, which is critical in enterprise analytics.

---

## 🧱 Full Architecture

### Frontend
- React + TypeScript  
- Recharts for stakeholder-friendly visualization  
- Interactive dashboard + retention simulation UI  

### Backend
- FastAPI REST API  
- Scikit-learn prediction service  
- Explainable output generation  

### Data
- Synthetic churn dataset with categorical + numeric features  
- Feature engineering to simulate customer behavioral signals  

---

## 🚀 Deployment & Infrastructure (Homelab Hosted)

This project is not only a machine learning demo — it is deployed as a real service.

### Deployment includes:

- Dockerized frontend + backend containers  
- Orchestrated using Docker Compose  
- Hosted on a personal Linux VM inside a home lab  
- Exposed securely to the internet using **Cloudflare Tunnel (HTTPS, no port forwarding)**  
- Accessible through a real domain:

➡️ **https://churn.luis-demo.com**

This deployment process mirrors production concerns such as:

- Service availability  
- Secure routing  
- Containerization  
- Real-world app hosting  

---

## ⚠️ Friendly Note (Campus Wi-Fi Reality)

Some university or corporate networks may block Cloudflare Tunnel traffic
(because they treat tunnels like suspicious portals to another dimension).

If the domain does not load on school Wi-Fi:

✅ Try switching networks or using a mobile hotspot  
✅ The app is always accessible internally through the VM/Tailscale setup  

---

## ✅ Features

- KPI cards (total customers, churn rate)  
- Segment churn charts by contract and internet type  
- Clickable customer table  
- Churn prediction + probability output  
- Explainable model factors (top feature weights)  
- Retention offer simulation (in progress)  

---

## 🛠️ Tech Stack

- React  
- TypeScript  
- FastAPI  
- Python  
- Scikit-learn  
- Docker + Docker Compose  
- Cloudflare Tunnel (deployment + HTTPS)  

---

## ▶️ Running Locally

### Backend
```bash
cd backend
source .venv/bin/activate
uvicorn main:app --reload --port 8000
```

### Frontend
```bash
cd frontend
npm install
npm run dev
```

## 🐳 Running with Docker (Recommended)
```bash
docker compose up --build -d
```

Then access:
- Frontend: http://localhost:3000
- Backend API: http://localhost:8000/docs

---

## 🎯 Why This Project

This demo was built to practice true end-to-end solution delivery:
- Data + feature engineering
- Machine learning + interpretability
- API design
- UI/UX for decision support
- Deployment + infrastructure ownership

## 📌 Next Steps
- Add Postgres to store retention offer history
- SHAP-style per-customer explanations
- Auth (SSO-style login via Authentik)
- Monitoring dashboards (Grafana + Prometheus)
- Full production frontend build with Nginx

---

Built by **Luis Ramirez**

Repository: **ML-Risk-Assessment-Project**
