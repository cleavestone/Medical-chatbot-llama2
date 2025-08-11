# End-to-end Medical Chatbot

# 🩺 Medical Chatbot with RAG (Retrieval-Augmented Generation)

This project is a **Flask-based Medical Chatbot** that leverages **LangChain**, **OpenAI**, and **Pinecone** to deliver intelligent, context-aware responses from a medical knowledge base. It uses **Retrieval-Augmented Generation (RAG)** to enhance the chatbot’s capabilities by retrieving relevant documents before generating answers.

---

## 📌 Features
- **Medical domain knowledge** powered by the Gale Encyclopedia of Medicine.
- **RAG pipeline**: Fetches relevant context from a vector database before generating answers.
- **LangChain integration** for retrieval and prompt orchestration.
- **Pinecone** as the vector database for document storage and retrieval.
- **Flask** for the backend API.
- **HTML/CSS** for a simple web-based chat interface.

---

## 🛠 Tech Stack
- **Backend:** Python, Flask
- **LLM:** OpenAI GPT
- **Embeddings:** OpenAI Embeddings
- **Vector Store:** Pinecone
- **Framework:** LangChain
- **Frontend:** HTML, CSS, JavaScript

---


---

## ⚙️ How It Works
1. **Document Loading & Indexing**  
   - Medical documents are processed and embedded using **OpenAI Embeddings**.
   - Embeddings are stored in **Pinecone** for efficient similarity search.

2. **Retrieval-Augmented Generation**  
   - When the user asks a question, the chatbot retrieves the most relevant documents from Pinecone.
   - LangChain feeds these documents into a **PromptTemplate** alongside the query.
   - The **OpenAI LLM** generates a final, context-aware answer.

3. **Flask Web Interface**  
   - The frontend (`chat.html`) sends user queries to the Flask backend.
   - Backend runs the RAG pipeline and returns the answer as JSON.
   - The frontend displays the response in the chat UI.

---

## 🚀 Installation & Setup
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/medical-chatbot-rag.git
cd medical-chatbot-rag

## Steps

**create virtual environment**
```bash
virtualenv mchaatbot
```
**activate virtual environment**
```bash
source mchatbot/scripts/activate
```
**install requirements.txt**
```bash
pip install -r requirements.txt
```
**Create  a .env file in the root directory and store your Pinecone API key and openai key**
```ini
PINECONE_API_KEY="XXXXXXXXXXXXXXXXXXXXXXXXX"
OPENAI_API_KEY="XXXXXXXXXXXXXXXXXXXXXXXXX"
```

```bash
python store_index.py
```

```bash
python app.py
```
```bash
open localhost
```
### Tech stack
- Python
- Langchain
- OpenAI
- Pinecone


