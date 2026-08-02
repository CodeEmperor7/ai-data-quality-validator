# AI Data Quality Validator

<p align="center">

![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.115-green)
![React](https://img.shields.io/badge/React-19-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/status-active-success)

</p>

<p align="center">

An enterprise-grade platform for validating, profiling, monitoring, and improving AI datasets used for machine learning and Large Language Model (LLM) applications.

</p>

---

# Overview

AI Data Quality Validator helps AI engineers ensure that datasets are clean, consistent, complete, and production-ready before model training or evaluation.

The platform automatically detects missing values, duplicate records, inconsistent annotations, schema violations, formatting issues, label imbalance, data drift, and other quality problems.

Designed for AI teams, the application supports structured, semi-structured, and annotation datasets while providing detailed validation reports and quality metrics.

---

# Features

## Dataset Validation

Validate datasets before training or deployment.

Supported checks

- Missing values
- Duplicate records
- Invalid data types
- Schema validation
- Required fields
- Null detection
- Empty values
- Invalid formats

---

## Annotation Validation

Validate annotation quality for AI datasets.

Supports

- Classification
- Named Entity Recognition
- Object Detection
- Image Segmentation
- OCR
- Text Classification
- LLM Evaluation Datasets

---

## Schema Validation

Automatically verify dataset structure.

```
Dataset

↓

Schema Validation

↓

Field Validation

↓

Data Type Validation

↓

Quality Report
```

---

## Data Profiling

Generate statistics including

- Row count
- Column count
- Missing percentage
- Unique values
- Cardinality
- Distribution
- Outliers

---

## Duplicate Detection

Detect

- Exact duplicates
- Near duplicates
- Duplicate prompts
- Duplicate responses
- Similar records

---

## Label Distribution

Visualize label balance.

```
Dataset

↓

Class Distribution

↓

Imbalance Detection

↓

Recommendations
```

---

## Data Drift Detection

Compare datasets over time.

```
Training Data

↓

Production Data

↓

Distribution Comparison

↓

Drift Report
```

---

## Quality Scoring

Generate an overall quality score based on

- Completeness
- Consistency
- Accuracy
- Validity
- Uniqueness
- Integrity

---

## Report Generation

Export reports as

- PDF
- CSV
- Excel
- JSON

---

# Architecture

```
                Web Dashboard

                      │

                      ▼

               FastAPI Backend

      ┌─────────────┼─────────────┐

      ▼             ▼             ▼

 Dataset API   Validation Engine  Reports

      │             │             │

      └─────────────┼─────────────┘

                    ▼

            Data Processing

                    ▼

           Quality Analysis

                    ▼

           Validation Report
```

---

# Technology Stack

## Frontend

- React
- TypeScript
- Tailwind CSS

---

## Backend

- Python
- FastAPI
- Pydantic

---

## Data Processing

- Pandas
- NumPy
- Great Expectations

---

## Database

- PostgreSQL
- SQLite

---

## Visualization

- Plotly
- Chart.js

---

## DevOps

- Docker
- GitHub Actions

---

# Project Structure

```
ai-data-quality-validator/

├── app/
│   ├── api/
│   ├── validators/
│   ├── profiling/
│   ├── reports/
│   ├── analytics/
│   ├── services/
│   ├── database/
│   ├── models/
│   └── utils/
│
├── datasets/
├── reports/
├── tests/
├── frontend/
├── docs/
├── scripts/
└── README.md
```

---

# Installation

Clone the repository

```bash
git clone https://github.com/ForwardAva/ai-data-quality-validator.git
```

Navigate to the project

```bash
cd ai-data-quality-validator
```

Create a virtual environment

```bash
python -m venv .venv
```

Activate the environment

Windows

```bash
.venv\Scripts\activate
```

Linux / macOS

```bash
source .venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# Environment Variables

Create a `.env` file.

```env
DATABASE_URL=

JWT_SECRET=

REPORT_OUTPUT=reports/

MAX_UPLOAD_SIZE=100MB
```

---

# Quick Start

Run the backend

```bash
uvicorn app.main:app --reload
```

Run the frontend

```bash
npm install

npm run dev
```

Open your browser

```
http://localhost:3000
```

---

# Supported Dataset Formats

- CSV
- JSON
- JSONL
- Excel
- Parquet
- TSV

---

# Core Features

- Dataset Validation
- Annotation Validation
- Data Profiling
- Schema Validation
- Data Drift Detection
- Duplicate Detection
- Quality Reports
- Analytics Dashboard

---

## Next Section

- REST API
- Dataset Upload API
- Validation API
- Report API
- Docker
- Testing
- CI/CD
- Deployment
- Roadmap
- Contributing
- License

---

# REST API

Run the API server

```bash
uvicorn app.main:app --reload
```

Base URL

```
http://localhost:8000
```

Swagger Documentation

```
http://localhost:8000/docs
```

ReDoc

```
http://localhost:8000/redoc
```

---

# API Endpoints

## Upload Dataset

```
POST /api/v1/datasets/upload
```

Supported formats

- CSV
- JSON
- JSONL
- Excel
- Parquet
- TSV

Response

```json
{
  "dataset_id": "b52d9f41",
  "status": "uploaded"
}
```

---

## Validate Dataset

```
POST /api/v1/validation/run
```

Request

```json
{
  "dataset_id": "b52d9f41",
  "validation_profile": "standard"
}
```

Response

```json
{
  "status": "completed",
  "quality_score": 96.8
}
```

---

## Dataset Profile

```
GET /api/v1/datasets/{id}/profile
```

Returns

- Row count
- Column count
- Missing values
- Duplicate rows
- Column statistics
- Data types

---

## Quality Report

```
GET /api/v1/reports/{id}
```

Returns a complete validation report.

---

## Export Report

```
POST /api/v1/reports/export
```

Supported formats

- PDF
- CSV
- Excel
- JSON

---

## Detect Data Drift

```
POST /api/v1/drift/analyze
```

Compare two datasets.

Request

```json
{
  "baseline_dataset":"dataset_a",
  "current_dataset":"dataset_b"
}
```

---

## Annotation Validation

```
POST /api/v1/annotations/validate
```

Supported tasks

- Classification
- NER
- OCR
- Image Classification
- Object Detection
- LLM Evaluation
- Question Answering

---

# Validation Workflow

```
Upload Dataset

        │

        ▼

Schema Validation

        │

        ▼

Data Profiling

        │

        ▼

Quality Checks

        │

        ▼

Validation Report

        │

        ▼

Export Results
```

---

# Validation Rules

The platform validates

- Missing Values
- Duplicate Records
- Invalid Data Types
- Invalid Labels
- Empty Columns
- Invalid Dates
- Schema Violations
- Label Imbalance
- Data Drift
- Outliers

---

# Example Repository Structure

```
app/

├── api/

├── analytics/

├── database/

├── profiling/

├── reports/

├── schemas/

├── services/

├── validators/

├── middleware/

├── utils/

└── main.py
```

---

# Testing

Run all tests

```bash
pytest
```

Run coverage

```bash
pytest --cov=app
```

Run validation tests

```bash
pytest tests/validation
```

---

# Docker

Build

```bash
docker build -t ai-data-quality-validator .
```

Run

```bash
docker run -p 8000:8000 ai-data-quality-validator
```

Docker Compose

```bash
docker compose up -d
```

---

# Performance

| Metric | Result |
|---------|-------:|
| Dataset Upload | < 2 sec |
| Validation Speed | 100K+ rows/min |
| Duplicate Detection | < 1 sec |
| API Latency | < 400 ms |
| Concurrent Users | 500+ |

---

# Screenshots

Replace these placeholders with your own screenshots.

```
docs/images/dashboard.png

docs/images/upload.png

docs/images/profile-report.png

docs/images/validation-results.png

docs/images/data-drift.png

docs/images/analytics.png
```

---

# Roadmap

## Version 1.0

- [x] Dataset Upload
- [x] Schema Validation
- [x] Data Profiling
- [x] Duplicate Detection
- [x] Quality Reports
- [x] REST API

## Version 1.1

- [ ] Scheduled Validation
- [ ] Batch Processing
- [ ] Dataset Versioning
- [ ] Team Collaboration
- [ ] Email Notifications

## Version 2.0

- [ ] AI Data Cleaning
- [ ] Automatic Error Correction
- [ ] Active Learning Integration
- [ ] Real-Time Monitoring
- [ ] Enterprise Workspaces
- [ ] Data Lineage
- [ ] ML Dataset Registry
- [ ] Cloud Storage Integration

---

# Contributing

Contributions are welcome.

1. Fork the repository.

2. Create a feature branch.

```bash
git checkout -b feature/my-feature
```

3. Commit your changes.

```bash
git commit -m "Add custom validation rule"
```

4. Push your branch.

```bash
git push origin feature/my-feature
```

5. Open a Pull Request.

---

# Security

Never commit sensitive datasets, API keys, or credentials.

Use environment variables for secrets and follow secure data handling practices.

---

# License

This project is licensed under the MIT License.

See the `LICENSE` file for details.

---

# Author

**Oscar Garcia**

**AI Quality Engineer • LLM Evaluation Specialist • AI Application Developer**

GitHub

https://github.com/ForwardAva

---

# Future Enhancements

- AI-Based Data Cleaning
- Custom Validation Rules
- LLM Dataset Validation
- Prompt Dataset Analysis
- Annotation Consensus Scoring
- Data Version Control
- Automated Dataset Monitoring
- Cloud Storage Connectors
- Model Readiness Score
- Enterprise Audit Logs

---

# Support

If you find this project useful, consider giving it a ⭐ on GitHub.

Bug reports, feature requests, and pull requests are always welcome.

---

<p align="center">

Built with ❤️ using FastAPI, React, Pandas, Great Expectations, and Python.

</p>