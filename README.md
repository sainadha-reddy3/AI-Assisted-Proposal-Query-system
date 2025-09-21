# AI-Assisted Proposal Query System 🚀

> **Internship Project — National Remote Sensing Centre (NRSC), ISRO**  
> Role: Python Developer & AI Integration (June 2025 – September 2025)  
> Author: Kasina Naga Sainadha Reddy

---

## 📖 Overview

The **AI-Assisted Proposal Query System** is a secure document processing pipeline developed during my internship at **ISRO–NRSC**.  

It digitizes and manages research proposals by:
- Handling **PDF, DOCX, and scanned image** formats
- Performing **OCR extraction** for scanned files
- Using a **local LLM (Mistral via Ollama)** for metadata and field extraction
- Storing structured outputs in **PostgreSQL**
- Providing a **React-based frontend** for uploads, querying, and review

This system was designed for **offline deployment in ISRO’s Virtual Machine environment**, ensuring compliance with organizational data security requirements.

---

## 🏗️ System Architecture

### Backend (FastAPI + Python)
- File upload and ingestion endpoints
- Asynchronous OCR + AI parsing pipelines
- Schema validation and error handling via **SQLAlchemy + Pydantic**
- Secure transactional storage in **PostgreSQL**

### OCR & AI Extraction
- **Tesseract OCR** for scanned images
- **Poppler** for PDF processing
- **Mistral LLM** via **Ollama** (offline, local inference)
- Hybrid **rule-based + AI extraction** for reliability

### Database (PostgreSQL 17)
- Central schema with:
  - `documents` (raw input)
  - `extracted_metadata` (structured fields)
  - `logs` (pipeline tracking)

### Frontend (React + Node.js)
- Upload and query interface
- Search, filter, and validation dashboard
- Status tracking for uploaded proposals

---

## ⚙️ Tech Stack

- **Language:** Python 3.11  
- **Backend:** FastAPI  
- **Database:** PostgreSQL 17  
- **ORM:** SQLAlchemy  
- **OCR:** Tesseract OCR + Poppler  
- **AI Model:** Mistral (via Ollama)  
- **Frontend:** React (Node.js LTS)  
- **Deployment:** ISRO Secure Virtual Machine  

---

## 🔑 Key Features

- 📂 Upload proposals in multiple formats  
- 🔎 OCR text extraction (scanned PDFs/images)  
- 🤖 AI-powered field extraction with Mistral  
- 💾 Structured storage in PostgreSQL  
- 🖥️ Query and review interface in React  
- 🔒 Offline, secure, VM-only deployment  

---

## 🚀 Installation Guide

### 1. Core Tools
- [Python 3.11](https://www.python.org/downloads/)
- [PostgreSQL 17](https://www.postgresql.org/download/)
- [Node.js LTS](https://nodejs.org/en/download)

### 2. OCR & AI
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- [Poppler](https://poppler.freedesktop.org/)
- [Ollama](https://ollama.com/) with Mistral model

### 3. Python Dependencies
```bash
pip install fastapi uvicorn sqlalchemy psycopg2-binary pydantic
pip install python-multipart pillow
4. React Frontend
bash
Copy code
cd frontend
npm install
npm run dev     # for development
npm run build   # for production
📂 Project Structure
graphql
Copy code
AI-Assisted-Proposal-Query-System/
│
├── backend/
│   ├── app/
│   │   ├── main.py            # FastAPI entrypoint
│   │   ├── routes/            # API routes
│   │   ├── services/          # OCR + AI modules
│   │   └── db/                # SQLAlchemy models
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   │   ├── pages/UploadPage.tsx
│   │   ├── components/
│   │   └── services/api.ts
│   └── package.json
│
├── database/
│   └── schema.sql             # PostgreSQL schema
│
└── README.md
📊 Workflow
Upload proposal (PDF, DOCX, Image) → via React frontend

OCR extraction → Tesseract + Poppler in FastAPI pipeline

AI metadata parsing → Local Mistral model (Ollama)

Storage → PostgreSQL schema validation + logging

Query & review → React dashboard for ISRO reviewers

🔒 Security
Fully offline — no external API calls

Deployed inside secure ISRO VMs

Database credentials restricted to local config

Logs maintained for transparency and debugging

📌 Future Enhancements
Advanced LLM fine-tuning for ISRO-specific proposal formats

Role-based access control for reviewers

Extended analytics dashboards (proposal trends, statistics)

Integration with ISRO’s internal workflow management systems

👨‍💻 Author
Kasina Naga Sainadha Reddy
