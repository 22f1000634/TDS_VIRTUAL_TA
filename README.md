
# 🤖 TDS Virtual TA

**TDS Virtual TA** is an AI-powered assistant built using Retrieval-Augmented Generation (RAG). It helps students in the IITM BSc program get accurate answers to academic questions using Discourse posts and course materials. You can ask text-based questions or upload an image (e.g., screenshot of an assignment) and receive AI-generated responses with proper source links.
> 🔥 Live Demo: [https://tds-virtual-ta-0etl.onrender.com](https://tds-virtual-ta-0etl.onrender.com)
---

## ✨ Features

- 💬 Natural language Q&A
- 🖼 Image-based question support (via GPT-4o vision)
- 🔎 RAG pipeline using Discourse + Markdown content
- 📚 Exact sources shown with every answer
- ⚡ FastAPI backend with Bootstrap-based UI

---

## 📁 Project Structure

```
.
├── scrape_discourse.py
├── scrape_course.py
├── app.py               # FastAPI backend with API + UI routes
├── index.html           # Chatbot frontend UI
├── preprocess.py        # Script to process and embed course data
├── knowledge_base.db    # SQLite DB containing embedded chunks
├── requirements.txt     # Python dependencies
└── LICENSE              # MIT License
```

---

## 🚀 How to Start by Code

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/tds-virtual-ta.git
cd tds-virtual-ta
```

---

### 2. Install Python Dependencies

```bash
pip install -r requirements.txt
```

---

### 3. Set Your API Key

Create a `.env` file in the root folder with the following content:

```
API_KEY=your_openai_or_aipipe_key
```

---

### 4. Preprocess the Knowledge Base (One Time)

This script fetches and embeds Discourse and Markdown data into `knowledge_base.db`.

```bash
python preprocess.py
```

---

### 5. Run the Server

```bash
uvicorn app:app --reload
```

Once running, visit:
```
http://127.0.0.1:8000
```

---

### 6. Ask Questions!

Open your browser → type your question → optionally attach an image → click "Send".

You’ll get a rich answer with source links backed by real Discourse or doc content.

---

## 📘 Sources Used

- IITM Online Discourse posts
- Markdown documents from the official student portal
- Embeddings generated using OpenAI-compatible APIs

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

Built by **Raj** — for IITM students who want quick, smart, and reliable answers.
