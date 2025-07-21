# 🧠 UPSC Question Paper Generator AI Agent

This is a production-ready AI-powered RAG (Retrieval Augmented Generation) system that generates new UPSC GS questions by learning from previous year question papers (PYQs). Built with `LangChain`, `ChromaDB`, `Ollama`, and `Gradio`.

---

## 🚀 Features

- 🔍 Parses and extracts PYQs from PDFs.
- 🧠 Vectorizes and stores questions using ChromaDB.
- 📚 Tags questions based on GS paper structure.
- 🧪 Generates new UPSC-style questions using local LLMs via Ollama.
- 💻 Intuitive Gradio interface for interaction.
- 🗃️ Organized modular structure for clarity and scalability.

---

## 📁 Project Structure

upsc-agent/
│
├── pyq_data/ # Input PDFs of GS papers
├── data/ # Processed data and vector store
│ ├── chunks.json
│ ├── tagged_questions.json
│ └── chroma_db/
│
├── supabase.env # Your Supabase keys (gitignored)
├── parse_papers.py # PDF parsing logic
├── tag_questions.py # Tagging logic
├── vector_store.py # ChromaDB vectorization
├── generate_questions.py # AI generation using Ollama
├── app.py # Gradio interface
├── requirements.txt # Python dependencies
├── .gitignore
└── README.md


---

## ⚙️ Setup Instructions

### 1. 🛠️ Install Dependencies

```bash
pip install -r requirements.txt

2. 📦 Install & Set Up Ollama

    Download Ollama.

    Start the Ollama server:

ollama serve

    Pull your desired model (e.g., phi3):

ollama pull phi3

    💡 Or link existing models via environment variable:

export OLLAMA_MODELS="/path/to/ollama/models"

3. 🔍 Add UPSC PDFs

Place UPSC GS PDFs in pyq_data/ folder. Ensure filenames include the year for parsing logic to work correctly.
🧪 Run Components
➤ Parse PDFs

python parse_papers.py

➤ Tag Questions (e.g., GS1/GS2)

python tag_questions.py

➤ Build Vector Store

python vector_store.py

➤ Generate New Questions

python generate_questions.py

➤ Run the UI (Gradio)

python app.py

Then open the link shown in your terminal to interact with the app.
🧠 Tech Stack
Tool	Purpose
Python	Core logic
Ollama	Local LLM execution
LangChain	Prompt chaining and orchestration
ChromaDB	Vector database for RAG
Gradio	Frontend interface
PyMuPDF	PDF parsing
Supabase	(Optional) Key storage
📌 Todo & Ideas

Add tagging by theme (e.g., Geography, Ethics, etc.)

Integrate Supabase for cloud sync

Add Mistral or Code Llama support

Export generated questions as PDFs

    Add API support for integration with other platforms

👨‍💻 Author

Hardhik M
📫 GitHub
🪪 License

This project is licensed under the MIT License.
