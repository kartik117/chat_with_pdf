# Chat with PDF

<img width="2356" height="1260" alt="image" src="https://github.com/user-attachments/assets/c0f6cb0e-9f86-4525-b202-ad98f7c9b624" />


A Streamlit app that lets you upload a PDF and ask questions about its content. It uses [embedchain](https://github.com/embedchain/embedchain) to chunk and embed the PDF into a local vector database (Chroma), then answers your questions using a locally-running [Ollama](https://ollama.com/) LLM (`llama3.2`) — no API keys or cloud costs required.

## Features

- Upload and preview a PDF directly in the browser
- Index the PDF into a local vector store for semantic search
- Chat interface to ask questions grounded in the PDF's content
- Runs fully locally (Ollama for both the LLM and embeddings)

## Prerequisites

- Python 3.9+
- [Ollama](https://ollama.com/download) installed and running locally
- The `llama3.2` model pulled:
  ```
  ollama pull llama3.2
  ```

## Setup

1. Clone the repo:
   ```
   git clone https://github.com/kartik117/chat_with_pdf.git
   cd chat_with_pdf
   ```
2. Create and activate a virtual environment:
   ```
   python3 -m venv venv
   source venv/bin/activate
   ```
3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

## Usage

Make sure Ollama is running, then start the app:

```
streamlit run chat_pdf.py
```

Open the URL Streamlit prints (typically `http://localhost:8501`), upload a PDF, click **Add to Knowledge Base**, and start asking questions about it.

## Tech stack

- [Streamlit](https://streamlit.io/) — web UI
- [embedchain](https://github.com/embedchain/embedchain) — RAG pipeline (chunking, embeddings, retrieval)
- [Chroma](https://www.trychroma.com/) — local vector database
- [Ollama](https://ollama.com/) — local LLM and embedding model runtime

## License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.
