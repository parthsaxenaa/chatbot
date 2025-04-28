
# 🌸 Ritual Guide Chatbot 🤖

A **Google Colab-based chatbot** that answers your questions about Indian rituals, festivals, and traditions using smart document analysis. Powered by **LangChain**, **FAISS**, and **HuggingFace embeddings** for a seamless, semantic search experience.

---

## ✨ Features
- 🛕 Answers queries about **Indian festivals, rituals, and regional traditions**  
- 📄 Processes **PDF** and **TXT** documents  
- 🧠 Uses **HuggingFace's `all-MiniLM-L6-v2` model** for embeddings  
- ⚡ **FAISS vector database** for efficient similarity search  
- 💬 **Interactive chat interface** for smooth conversations  

---

## ⚙️ Installation & Setup

### 1. Install Requirements
```bash
pip install langchain-community faiss-cpu sentence-transformers pypdf
```

### 2. Upload Documents
- Upload your **ritual-related PDF/TXT** files when prompted in the Colab notebook.
- Example supported file: `ritual_guide_india.txt`

> 🗂️ **Supported formats**: `.pdf`, `.txt`

---

## 🚀 Usage

```python
# Initialize the chatbot
chatbot = ColabChatbot()

# Start chatting
while True:
    query = input("Your question: ")
    if query.lower() in ["exit", "quit", "bye"]:
        break
    print("Answer:", chatbot.ask(query))
```

---

## 💬 Example Interaction

```
Your question: kerala

Answer:
2.3. Regional Rituals
- Theyyam (Kerala): A ritualistic performance where the performer is believed to become a deity.
- Garudan Thookam (Kerala): Devotees perform a ritual dance and are hung from hooks as an offering.
```

---

## 🔑 Key Components
- `ColabChatbot` class for **document processing** and **query handling**
- **Text splitting**: 1000-character chunks with 200-character overlap
- **Top 2 relevant document segments** returned per query
- **Multi-file support** via **LangChain loaders**

---

## 📦 Dependencies

```python
langchain-community == 0.0.11
faiss-cpu == 1.7.4
sentence-transformers == 2.2.2
pypdf == 3.17.0
```

---

## 📄 License

**MIT License**  
Free for **educational** and **research** use.

> ⚡ **Note**: Designed specifically for the **Google Colab environment**.  
> 🛕 Please **upload your ritual documents** before interacting with the chatbot.

---
