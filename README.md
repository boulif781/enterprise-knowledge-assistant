# AI Powered Enterprise Knowledge Assistant

> An AI-powered Enterprise Knowledge Assistant that enables employees to retrieve information from enterprise documents using Retrieval-Augmented Generation (RAG) while ensuring every response is grounded with source references.

---

##  Project Overview

The AI Powered Enterprise Knowledge Assistant is a microservice-based web application that allows users to upload enterprise documents (PDF, DOCX, CSV) and interact with them using natural language.

Instead of manually searching hundreds of pages, users can ask questions, and the system retrieves relevant document chunks using semantic search before generating accurate responses using a local Large Language Model (LLM).

### Key Objectives

- Reduce document searching time
- Improve employee productivity
- Ensure data privacy with offline AI
- Provide accurate answers with document references
- Support enterprise knowledge management

---

##  Architecture

> *(Replace this image after creating the architecture diagram.)*

```
                        +----------------------+
                        |     React (Vite)     |
                        +----------+-----------+
                                   |
                                   |
                        REST APIs (JWT)
                                   |
                     +-------------+-------------+
                     |      Spring Boot API      |
                     | Authentication            |
                     | User Management           |
                     | File Metadata             |
                     | Chat History              |
                     +-------------+-------------+
                                   |
                     REST APIs
                                   |
                  +----------------+----------------+
                  |         FastAPI AI Service      |
                  | Document Parsing                |
                  | Chunking                        |
                  | Embedding                       |
                  | Retrieval                       |
                  | Prompt Engineering              |
                  +---------+-----------+-----------+
                            |           |
                            |           |
                     ChromaDB       Ollama
                     Vector DB      Local LLM

                            |
                      PostgreSQL
```

---

##  Features

### Authentication

- JWT Authentication
- Role-based Access
- Secure Password Hashing (BCrypt)

### Document Management

- Upload PDF
- Upload DOCX
- Upload CSV
- Store document metadata
- Delete documents

### AI Knowledge Assistant

- Retrieval-Augmented Generation (RAG)
- Semantic Search
- Context-aware Responses
- Source Referencing
- Procedural Checklist Generation

### Chat

- Ask questions
- View AI responses
- Source citations
- Chat history

### Deployment

- Docker Compose
- Offline AI
- Local LLM using Ollama

---

##  Tech Stack

| Layer | Technology |
|---------|------------|
| Frontend | React + Vite |
| Backend | Spring Boot |
| Security | Spring Security + JWT |
| AI Service | FastAPI |
| AI Framework | LangChain |
| Embeddings | Sentence Transformers |
| Vector Database | ChromaDB |
| Database | PostgreSQL |
| LLM | Ollama |
| Deployment | Docker Compose |
| Version Control | Git + GitHub |

---

##  Folder Structure

```
enterprise-knowledge-assistant/

├── frontend/
├── backend/
├── ai-service/
├── database/
├── docker/
├── docs/
├── scripts/
│
├── .github/
│   ├── workflows/
│   ├── ISSUE_TEMPLATE/
│   └── PULL_REQUEST_TEMPLATE.md
│
├── docker-compose.yml
├── README.md
├── CHANGELOG.md
└── LICENSE
```

---

##  Installation

### Clone Repository

```bash
git clone https://github.com/<organization>/enterprise-knowledge-assistant.git
```

```bash
cd enterprise-knowledge-assistant
```

---

### Backend

```bash
cd backend
```

Run Spring Boot application.

---

### Frontend

```bash
cd frontend

npm install

npm run dev
```

---

### AI Service

```bash
cd ai-service

pip install -r requirements.txt

uvicorn app.main:app --reload
```

---

### Database

Install PostgreSQL and create the required database.

---

### Ollama

Install Ollama.

Download your preferred model.

Example:

```bash
ollama pull llama3.2
```

---

##  Running Locally

Start each service individually or use Docker Compose.

Example:

```
Frontend : http://localhost:5173

Backend : http://localhost:8080

AI Service : http://localhost:8000

Swagger : http://localhost:8080/swagger-ui/index.html
```

---

##  Docker Setup

Run the complete project

```bash
docker compose up --build
```

Services

- React Frontend
- Spring Boot Backend
- FastAPI AI Service
- PostgreSQL
- ChromaDB
- Ollama

---

##  API Documentation

Swagger UI

```
http://localhost:8080/swagger-ui/index.html
```

FastAPI Docs

```
http://localhost:8000/docs
```

---

##  Testing

### Backend

- JUnit

### Frontend

- React Testing Library

### AI Service

- Pytest

### API

- Postman

---

##  Development Workflow

```
GitHub Issue
      ↓
Feature Branch
      ↓
Development
      ↓
Unit Testing
      ↓
Pull Request
      ↓
Code Review
      ↓
Merge into develop
      ↓
Sprint Testing
      ↓
Release
```

---

##  Team Members

| Name | Responsibility |
|--------|----------------|
| Jayachandra | Spring Boot Backend, Docker, DevOps |
| Omraj | AI Service (FastAPI, LangChain, Ollama) |
| Sejal | React Frontend, Figma|
| Harshal | Database, Documentation, Reports |

---

##  Documentation

Project documentation is available in the `/docs` directory.

- Architecture
- API Documentation
- Database Design
- Deployment Guide
- Sprint Reports
- Developer Guide

---

## Contributing

1. Create a feature branch

```
feature/<feature-name>
```

2. Commit using Conventional Commits

Example

```
feat(auth): implement JWT authentication
```

3. Open a Pull Request to `develop`

4. Get at least one review approval

5. Merge after successful review

---

## License

This project is developed for academic purposes as a Final Year Engineering Project.
