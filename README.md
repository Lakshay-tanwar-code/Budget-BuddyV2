<div align="center">
  <img src="https://placehold.co/200x200?text=Budget+Buddy" alt="Budget Buddy Logo" width="200" />
  <h1>💼 Budget Buddy AI V2 🚀</h1>
  <p><strong>Your Ultimate Multimodal AI Financial Assistant</strong></p>

  [![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
  [![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
  [![Gemini](https://img.shields.io/badge/Google_Gemini-Flash-orange.svg)](https://aistudio.google.com/)
  [![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
  [![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
</div>

<br>

## 📖 Overview

**Budget Buddy AI V2** is a next-generation financial assistant powered by **FastAPI**, **Google Gemini**, **LangChain**, and **ChromaDB**. It is designed to act as your personal AI wealth manager, seamlessly blending real-time market data with cutting-edge Retrieval-Augmented Generation (RAG) and Multimodal AI capabilities. 

Whether you need to analyze a spreadsheet of expenses, extract insights from a complex financial PDF, fetch live stock market data, or just get some solid financial advice—Budget Buddy does it all with a sleek, interactive web interface.

---

## ✨ Key Features

- 🧠 **Multimodal AI Analysis:** Leverages Google's `gemini-1.5-flash` model to analyze raw text, CSV datasets, financial PDFs, and even images (receipts, invoices).
- 🔍 **RAG & Vector Search:** Uses **ChromaDB** and **LangChain** for robust document ingestion and context-aware responses, allowing you to "chat with your documents."
- 📈 **Real-Time Market Data:** Integrates `yfinance` to fetch live stock prices and market trends instantly.
- 🌍 **Web & News Scraping:** Automatically crawls the web using DuckDuckGo, BeautifulSoup, and Trafilatura to bring you the latest economic news and summarize web pages on the fly.
- 💱 **Live Exchange Rates:** Integrates the Frankfurter API for accurate currency conversion.
- ⚡ **High-Performance Backend:** Asynchronous Python backend powered by **FastAPI** for ultra-fast, streaming responses.
- 🐳 **Docker Ready:** Fully containerized for easy deployment to platforms like Render, Railway, or Google Cloud Run.

---

## 🛠️ Tech Stack

| Category | Technologies Used |
|----------|-------------------|
| **Backend** | Python, FastAPI, Uvicorn, Pydantic |
| **AI / LLMs** | Google Generative AI (Gemini Flash), LangChain, Sentence-Transformers |
| **Vector Database**| ChromaDB |
| **Data APIs** | yfinance, DuckDuckGo Search (DDGS), Frankfurter |
| **Document Processing**| Pandas (CSVs), PyPDF2 & pdfplumber (PDFs), Pillow (Images) |
| **Frontend** | HTML5, CSS3, Vanilla JS, Chart.js |

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- [Google Gemini API Key](https://aistudio.google.com/)
- Docker (optional, for containerized deployment)

### Local Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Lakshay-tanwar-code/Budget-BuddyV2.git
   cd Budget-BuddyV2
   ```

2. **Set up Virtual Environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables:**
   Create a `.env` file in the root directory and add your Gemini API Key:
   ```env
   GEMINI_API_KEY=your_api_key_here
   ```

5. **Run the Application:**
   ```bash
   uvicorn main:app --host 0.0.0.0 --port 8000
   ```
   Open your browser and navigate to `http://127.0.0.1:8000/static/index.html`.

### 🐳 Docker Deployment
You can easily deploy Budget Buddy using the included Dockerfile.
```bash
docker build -t budget-buddy-v2 .
docker run -p 8000:8000 budget-buddy-v2
```

---

## 📂 Project Architecture

- `main.py`: Core FastAPI application and API routes.
- `static/`: Frontend interface (`index.html`, `style.css`, `app.js`).
- `Dockerfile` & `.dockerignore`: Container configuration for production deployment.
- `chroma_db_gemini/`: Local vector database storage for RAG capabilities.
- `requirements.txt`: Python package dependencies.

---

## 💡 Usage Guide

1. **Launch the app** in your browser.
2. **Upload a document** (CSV, PDF, or image receipt) or type a financial query (e.g., *"What is the current stock price of AAPL?"*).
3. **Budget Buddy AI** will instantly ingest the data, query the vector database or live APIs if needed, and stream back a highly contextualized and accurate financial insight!

---
<div align="center">
  <i>Built with ❤️ for better financial management.</i>
</div>
