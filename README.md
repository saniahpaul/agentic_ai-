# 🎓 EduReach Platform

A full-stack **AI-powered college information and admission counseling platform** developed by **Sania H Paul** for helping students explore courses, fees, placements, and get branch recommendations based on their academic performance.

🔗 **Live Demo:** https://edu-reach-agentic-project.vercel.app/

---

## ✨ Features

* 🤖 **RAG-Based AI Chatbot**
  Answers student queries related to courses, fees, placements, and admission process.

* 📞 **AI Voice Counseling**
  Uses Vapi AI to call students, collect KCET rank and 12th marks, and provide personalized branch suggestions.

* 📧 **Automated Email Recommendations**
  Generates and sends personalized recommendation emails based on AI conversation transcripts.

* 📄 **Brochure Download**
  Allows students to download the complete college brochure.

* 🔍 **Vector Search Support**
  Uses MongoDB Atlas Vector Search for intelligent retrieval.

---

## 🚀 Tech Stack

### Frontend

* React 19
* TypeScript
* Vite
* Tailwind CSS v4
* React Router v7
* Axios
* Lucide React
* React Hot Toast

### Backend

* Node.js (v20+)
* Express v5
* TypeScript
* MongoDB Atlas
* Mongoose
* LangChain
* Google Gemini (Chat + Embeddings)
* Vapi AI
* bcryptjs
* JWT

---

## ⚙️ Prerequisites

Before running this project, make sure you have:

* Node.js v20+
* MongoDB Atlas account (Vector Search enabled)
* Google AI Studio API Key
* Vapi account (optional for voice features)

---

## 🛠️ Installation & Setup

### 1. Clone the Repository

```bash id="g1"
git clone https://github.com/saniahpaul/agentic_ai-.git
```

### 2. Install Frontend Dependencies

```bash id="g2"
cd edureach-platform/client
npm install
```

### 3. Install Backend Dependencies

```bash id="g3"
cd ../server
npm install
```

---

## 🔐 Environment Variables

Create a `.env` file inside the server folder:

```env id="g4"
PORT=5000
CLIENT_URL=http://localhost:5173

MONGODB_URI=mongodb+srv://<user>:<password>@cluster.mongodb.net/edureach_db

JWT_SECRET=your_super_secret_key
JWT_EXPIRES_IN=7d

GOOGLE_API_KEY=your_google_gemini_api_key

VAPI_API_KEY=your_vapi_api_key
VAPI_PHONE_NUMBER_ID=your_vapi_phone_number_id
VAPI_ASSISTANT_ID=your_vapi_assistant_id
```

---

## 🧠 MongoDB Atlas Vector Search Index

Use this vector index configuration:

```json id="g5"
{
  "fields": [
    {
      "numDimensions": 3072,
      "path": "embedding",
      "similarity": "cosine",
      "type": "vector"
    }
  ]
}
```

**Index Name:** `edureachvectorindex`

---

## ▶️ Running the Application

### Backend

```bash id="g6"
cd server
npm run dev
```

### Frontend

```bash id="g7"
cd client
npm run dev
```

---

## 🌐 Local URLs

* Frontend: http://localhost:5173
* Backend: http://localhost:5000

---

## 📦 Production Build

### Build Frontend

```bash id="g8"
cd client
npm run build
```

### Build Backend

```bash id="g9"
cd server
npm run build
npm start
```

---

## 👩‍💻 Developed by

**Sania H Paul**
B.E. Computer Science & Design
Mysore University

---

⭐ If you found this project useful, consider giving it a star!
