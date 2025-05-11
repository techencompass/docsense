# 🧠 DocSense: AI-Powered Document Analyzer

## 🔍 Project Title: **DocSense - Modular AI Pipeline with Hexagonal Architecture**

---

## 📌 Summary
**DocSense** is an intelligent document analysis platform that extracts, classifies, and summarizes text from structured and unstructured documents (PDFs, images, scanned contracts, etc.). Built using a **Hexagonal Architecture**, DocSense ensures modularity, testability, and adaptability for future integrations. The frontend is powered by **Next.js + Tailwind CSS**, and Firebase handles authentication, database, and file storage.

---

## 🚀 Features

### ✅ Core Functionalities
- 🖼️ OCR from image-based documents (PDF, JPG, PNG)
- 🔍 Document classification using AI (contracts, invoices, resumes, etc.)
- 📑 Text extraction, section detection, entity recognition
- 🧠 LLM-based summarization (OpenAI/Gemini APIs)
- 🔐 Secure file upload and authentication (Firebase Auth)
- 📊 Document history and metadata dashboard

### 🧱 Modular Architecture (Hexagonal)
- **Adapters (driven)**: Firebase Storage, REST API, Web UI
- **Ports (driving)**: AI Service Interface, Document Ingestor, Extractor
- **Core Domain**: Document, Summary, Classification, Pipeline Engine

---

## 🏗️ Tech Stack
### 🌐 Frontend:
- **Next.js 14** (App Router)
- **Tailwind CSS** for styling
- **Firebase Auth**
- **React Hook Form**

### 🔙 Backend:
- **Node.js** (Edge/Serverless Functions)
- **OpenAI / Google Vertex AI / Gemini API**
- **Firebase Firestore** (for metadata)
- **Firebase Storage** (for uploaded docs)

---

## 📦 Folder Structure
```bash
/frontend-docsense-next
  ├── app/
  ├── components/
  ├── styles/
  └── utils/

/backend-docsense-functions
  ├── functions/
      ├── extract-text.ts
      ├── classify-doc.ts
      ├── summarize.ts
  └── lib/
      └── ai-pipeline-core.ts (Hexagonal domain core)
```

---

## 📘 How It Works
1. **User uploads a document** → stored in Firebase Storage
2. **Trigger OCR & AI Classification** using cloud function
3. **AI Pipeline** extracts entities, identifies sections, and summarizes
4. **Result saved** in Firestore & displayed in dashboard

---

## 🧠 Design Principles
- **Hexagonal Architecture**: Clear separation of concerns for core logic and external integrations
- **AI as Plug-in**: Supports OpenAI/Gemini interchangeable pipelines
- **Secure by Design**: Firebase Auth, storage rules, input sanitization

---

## 🧪 Test Strategy
- Unit tests for pipeline engines and ports
- Mock tests for AI adapters
- Cypress for UI testing

---

## 📈 Observability
- Logging via Firebase Logs
- Analytics via Firebase Events
- Error boundary component in Next.js for client-side tracebacks

---







---

## 🔮 Future Enhancements
- Document comparison and diff view
- GPT-powered Q&A interface over document context
- SOC2 compliant audit trail
- Multi-user access controls (RBAC)

---

## 🔗 License
MIT
