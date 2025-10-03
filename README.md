🤖 AI-Powered Resume Screening and Ranking System

An end-to-end AI-powered recruitment tool that automatically screens and ranks candidate resumes against job descriptions. The system combines React.js (frontend), Node.js (middleware), and Python + FastAPI (NLP engine) to deliver a fast, interactive, and intelligent hiring assistant for recruiters.

🚀 Features
👤 Resume Upload & Screening

Upload multiple resumes in PDF/DOCX format

Input or paste a job description

Extracts resume text using PyPDF2, pdfplumber, and python-docx

🧠 AI/NLP Engine

Text preprocessing with NLTK & spaCy (tokenization, stopword removal, normalization)

Converts resumes and job description into TF-IDF vectors

Computes similarity scores with Cosine Similarity

(Optional) Sentence-BERT embeddings for advanced semantic matching

📊 Ranking & Visualization

Generates ranked candidates list with similarity scores

Results displayed in an interactive table + bar chart

Helps recruiters quickly identify the best-matching candidates

🔐 System Architecture

Frontend: React.js + Tailwind CSS + Recharts (modern UI + visualization)

Backend: Node.js + Express (file uploads, API routing)

AI Service: Python + FastAPI (resume parsing, NLP, ranking logic)

Communication: Axios (between frontend → backend → AI engine)

🛠️ Tech Stack

Frontend

React.js (Vite)

Tailwind CSS (styling)

Recharts / Chart.js (data visualization)

Axios (API calls)

Backend

Node.js + Express (middleware server)

Multer (resume uploads)

Axios (forwarding requests to NLP engine)

NLP Engine

Python + FastAPI (AI service)

Scikit-learn (TF-IDF + Cosine similarity)

NLTK / spaCy (text preprocessing)

PyPDF2 / pdfplumber / python-docx (resume parsing)

📂 Project Structure
ai-resume-ranker/
│── frontend/          # React.js app (UI)
│── backend/           # Node.js server (API & uploads)
│── nlp-service/       # Python FastAPI service (NLP logic)
│── README.md

⚙️ Installation & Setup
1️⃣ Clone the repository
git clone https://github.com/yourusername/ai-resume-ranker.git
cd ai-resume-ranker

2️⃣ Setup Frontend (React)
cd frontend
npm install
npm run dev


Runs on 👉 http://localhost:5173

3️⃣ Setup Backend (Node.js)
cd backend
npm install
node server.js


Runs on 👉 http://localhost:5000

4️⃣ Setup NLP Engine (FastAPI)
cd nlp-service
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate  # macOS/Linux
pip install -r requirements.txt
uvicorn main:app --reload --port 8000


Runs on 👉 http://localhost:8000

🔄 Workflow

Recruiter uploads resumes + job description via frontend.

Node.js backend accepts files and forwards them to Python NLP API.

FastAPI engine extracts text, applies preprocessing, and computes similarity.

Ranked results are sent back → displayed in a table + chart in the UI.


🔮 Future Enhancements

Integration with MongoDB/PostgreSQL to store past rankings

Docker support for containerized deployment

BERT/Sentence-BERT embeddings for advanced semantic search

Export candidate ranking as PDF/Excel reports


📜 License

This project is licensed under the MIT License – free to use and modify.
