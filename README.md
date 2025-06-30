
# 📘 RAG-based LLM with LangChain and Gradio

This notebook builds a simple conversational RAG (Retrieval-Augmented Generation) application using LangChain and Gradio. It processes local documents, indexes them using ChromaDB, and enables user interaction via a chat interface powered by OpenAI models.

## 📦 Dependencies

Make sure the following packages are installed:

```bash
pip install langchain langchain-openai langchain-chroma python-dotenv gradio
```

## 📁 Project Structure

- `.env` – Contains your OpenAI API key
- `vector_db/` – Folder where Chroma vector store is saved
- `data/` – Folder containing `.txt` documents to be loaded and embedded

## 🔧 Environment Setup

Create a `.env` file:

```env
OPENAI_API_KEY=your_openai_api_key
```

## 🔑 Key Components

- **Document Loading:**  
  Uses `DirectoryLoader` and `TextLoader` from LangChain to load text files.

- **Text Splitting:**  
  Applies `CharacterTextSplitter` to chunk long documents for embedding.

- **Vector Store:**  
  Stores document embeddings using Chroma for fast retrieval.

- **Conversational Chain:**  
  Uses `ConversationalRetrievalChain` with `ChatOpenAI` to power the chatbot.

- **Gradio UI:**  
  Simple Gradio interface for querying the RAG chatbot.

## 🚀 How to Run

1. Place your `.txt` documents inside a `data/` folder.
2. Run the notebook cells step by step.
3. The final cell launches a Gradio interface for chatting with the AI.

## 🧠 Variables & Parameters

- `model = "gpt-4o-mini"` – LLM used for the chatbot
- `db_name = "vector_db"` – Name of the Chroma vector store
- `text_splitter` – Configured with `chunk_size` and `chunk_overlap`
- `folders` – List of directories containing documents
