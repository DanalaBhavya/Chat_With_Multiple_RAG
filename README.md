
# 📄 Chat with Multiple PDFs using Gemini (RAG)

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline that allows you to **chat with multiple PDF documents** using **Google Gemini Pro**.
You can upload PDFs, and the app will extract text, create embeddings, store them in a FAISS vector database, and answer your questions based on the retrieved context.

---

## 🚀 Features

* Upload **multiple PDFs** at once
* Extract and split text into **chunks**
* Generate **vector embeddings** using Google Generative AI
* Store embeddings in a **FAISS vector database**
* Retrieve the most relevant chunks during query time
* Answer questions using **Gemini-Pro** with context-aware responses
* Built with **Streamlit** for an interactive UI

---

## 🛠️ Tech Stack

* [Streamlit](https://streamlit.io/) – Frontend
* [LangChain](https://www.langchain.com/) – RAG pipeline
* [FAISS](https://github.com/facebookresearch/faiss) – Vector database
* [Google Generative AI](https://ai.google.dev/) – LLM & Embeddings
* [PyPDF2](https://pypi.org/project/pypdf2/) – PDF text extraction

---

## 📂 Project Structure

```
📁 chat-with-pdf
│── app.py              # Main Streamlit app
│── requirements.txt    # Dependencies
│── .env                # Google API key (not committed)
│── faiss_index/        # Vector store files (generated after processing PDFs)
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/chat-with-pdf.git
cd chat-with-pdf
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Add Environment Variable

Create a `.env` file in the project root:

```
GOOGLE_API_KEY=your_google_api_key_here
```

### 5️⃣ Run the App

```bash
streamlit run app.py
```

---

## 📘 How It Works (RAG Flow)

1. **Upload PDFs** → Extracts text using PyPDF2
2. **Text Splitting** → Breaks text into chunks with overlap
3. **Embedding** → Converts chunks into embeddings using `models/embedding-001`
4. **Vector Store** → Saves embeddings in **FAISS**
5. **Retrieval** → Finds the most relevant chunks for a user query
6. **Generation** → Feeds chunks + query into **Gemini-Pro** for the final answer

---

## 🎯 Example Use Cases

* Research assistance
* Summarizing academic papers
* Extracting insights from reports
* Conversational Q&A over documentation

---

## 📜 License

This project is licensed under the MIT License.

---

⚡ Built with ❤️ using **RAG + Gemini**

---
