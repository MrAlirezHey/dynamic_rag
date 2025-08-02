
# 🤖 Dynamic RAG Chatbot with PDF Support

Welcome to the **Dynamic RAG (Retrieval-Augmented Generation) Chatbot**!  
This powerful tool enables you to build a chatbot that can answer questions based on the content of PDF documents you provide.

Built with **Python**, using the **LangChain** framework for orchestration and **Gradio** for an intuitive web interface.

---

## ✨ Features

- 📤 **Dynamic Knowledge Base**: Instantly feed knowledge to the chatbot by uploading one or more PDF files.
- 💬 **Interactive UI**: Simple and user-friendly interface with Gradio.
- 🧠 **Conversational Memory**: Remembers the context of the current conversation for natural follow-ups.
- 🔍 **Advanced Retrieval**: Uses a `MultiQueryRetriever` to improve the quality of information retrieved.
- 🚀 **Easy to Set Up**: Minimal steps to get it running locally.

---

## ⚙️ How It Works

The application follows a **Retrieval-Augmented Generation (RAG)** architecture:

1. **📤 File Upload**: Upload PDFs through the Gradio interface.
2. **📄 Document Chunking**: Uses `PyPDFLoader` + `RecursiveCharacterTextSplitter` to break content into chunks.
3. **🔢 Embedding & Indexing**: Converts chunks into vector representations using OpenAI embeddings and stores them in **ChromaDB**.
4. **❓ Query & Retrieval**: Retrieves relevant chunks based on your question using semantic search.
5. **🧠 LLM Generation**: The question + retrieved text + chat history go to `gpt-4o-mini`, generating a grounded, contextual response.
6. **💬 Response**: Answer is shown in the chat interface.

---

## 🛠️ Technology Stack

| Layer              | Tech Used               |
|-------------------|-------------------------|
| Backend           | Python                  |
| Orchestration     | LangChain               |
| Web UI            | Gradio                  |
| Vector Database   | ChromaDB                |
| LLM & Embeddings  | OpenAI (GPT-4o-mini)    |
| PDF Processing    | PyPDFLoader             |

---

## 🚀 Getting Started

Follow these instructions to run the project locally.

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### 2. Create a Virtual Environment

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

**If you don't have a `requirements.txt`, create one with the following:**

```text
gradio
langchain
langchain-community
langchain-openai
chromadb
pypdf
tiktoken
```

### 4. Configure Your API Key

Edit the Python script (e.g., `app.py` or `Dynamic_RAG.ipynb`) and set your OpenAI API key:

```python
AI_token = 'YOUR_API_KEY_HERE'
```

> **Note**: The script uses a custom base URL (`https://api.gapgpt.app/v1`). If you're using the official OpenAI API, remove the `base_url` parameter.

---

### 5. Run the Application

```bash
python your_script_name.py
```

The Gradio interface will launch at:  
**http://127.0.0.1:7860**

---

## ▶️ How to Use the Chatbot

1. **Launch the App**: Run the script and open the browser at the shown URL.
2. **Upload PDFs**: Drag and drop your PDF files or click to browse.
3. **Build Knowledge Base**: Click **"Build vector"** and wait for the ✅ confirmation.
4. **Ask Questions**: Start chatting! Your answers are now grounded in the uploaded documents.

---

## 📄 License

MIT License.  
Feel free to use, modify, and share.

---

## 🌐 Contributions

Pull requests are welcome! If you'd like to contribute, feel free to fork this repo and submit improvements.

---


