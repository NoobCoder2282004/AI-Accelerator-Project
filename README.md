# AI Resume Screener - 

An AI-powered ATS (Applicant Tracking System) Resume Screener built using Flask, Sentence Transformers, and PDF Resume Parsing.

This project analyzes uploaded resumes against a Machine Learning Engineer Job Description and provides:

- Match Score
- Resume Ranking
- Skill Matching
- Missing Skills Detection
- Shortlisted / Maybe / Rejected Verdict
- Modern ATS-style UI

---

#  Features

- Upload multiple PDF resumes
- Extract resume text using pdfplumber
- Semantic similarity scoring using Sentence Transformers
- Skill-gap analysis
- Display rejection reasons
- Beautiful responsive UI
- Automatic resume ranking

---

#  Tech Stack

| Technology | Purpose |
|------------|---------|
|   Python   | Backend |
|    Flask   | Web Framework |
| Sentence Transformers | Semantic similarity |
| pdfplumber | PDF text extraction |
| HTML/CSS/JS | Frontend |
| Google Colab | Deployment/testing |

---

# How It Works

## 1. Resume Upload
Users upload PDF resumes through the web interface.

## 2. PDF Parsing
The backend extracts text from resumes using pdfplumber.

## 3. Semantic Similarity
The project uses the `all-MiniLM-L6-v2` Sentence Transformer model to compare resumes with the Job Description.

Similarity is calculated using cosine similarity.

## 4. Skill Matching
The system checks whether required skills are present in the resume.

Example skills:
- Python
- TensorFlow
- Docker
- SQL
- Kubernetes
- Flask
- PyTorch

## 5. Verdict Generation

| Score | Verdict |
|---|---|
| ≥ 55 + enough skills | Shortlisted |
| ≥ 45 | Maybe |
| Otherwise | Rejected |

---

# Project Structure

```bash
AI-Resume-Screener/
│
├── templates/
│   └── index.html
│
├── app.py
│
├── requirements.txt
│
└── README.md
