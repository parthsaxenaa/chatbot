```markdown
# Ritual Guide Chatbot 🤖

A Google Colab-based chatbot that answers questions about Indian rituals and traditions using document analysis. Built with LangChain and FAISS for semantic search capabilities.

## Features ✨
- Answers queries about Indian festivals, rituals, and regional traditions
- Processes both PDF and TXT documents
- Uses HuggingFace's `all-MiniLM-L6-v2` model for embeddings
- FAISS vector database for efficient similarity search
- Interactive chat interface

## Installation & Setup ⚙️

1. **Requirements**:
```bash
pip install langchain-community faiss-cpu sentence-transformers pypdf
```

2. **Upload Documents**:
- Upload your ritual-related PDF/TXT files when prompted by the notebook
- Supported files: `ritual_guide_india.txt` (example shown in notebook)

## Usage 🚀
```python
# Initialize chatbot
chatbot = ColabChatbot()

# Start interaction
while True:
    query = input("Your question: ")
    if query.lower() in ["exit", "quit", "bye"]:
        break
    print("Answer:", chatbot.ask(query))
```

## Example Interaction 💬
```
Your question: kerala

Answer: 
2.3. Regional Rituals
- Theyyam (Kerala): A ritualistic performance where the performer is believed to become a deity.
- Garudan Thookam (Kerala): Devotees perform a ritual dance and are hung from hooks as an offering.
```

## Key Components 🔑
- `ColabChatbot` class handles document processing and queries
- Text splitting: 1000-character chunks with 200-character overlap
- Returns top 2 most relevant document segments
- Supports multiple file types through LangChain loaders

## Dependencies 📦
```python
langchain-community == 0.0.11
faiss-cpu == 1.7.4
sentence-transformers == 2.2.2
pypdf == 3.17.0
```

## License 📄
MIT License - Free for educational and research use

> **Note**: Designed for Google Colab environment. Upload your ritual documents before querying.
```

This README provides:
1. Clear setup instructions
2. Usage examples
3. Technical specifications
4. Interactive elements with emoji visuals
5. Code blocks for easy copy-paste
6. Key feature highlights
7. Dependency requirements

The structure helps users quickly understand both the functional aspects and technical implementation of the chatbot.
