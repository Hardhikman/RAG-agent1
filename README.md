# 🧠 UPSC Question Paper Generator AI Agent

A production-ready RAG (Retrieval Augmented Generation) pipeline to generate new UPSC GS questions from PYQs using local LLMs like `phi3` or `mistral` via [Ollama](https://ollama.com), powered by `LangChain`, `ChromaDB`, and `Gradio`.

---

## 🚀 Features

- 🔍 Extracts questions from UPSC GS PDF files.
- 🏷️ Tags questions by year and paper (e.g., GS1, GS2).
- 📚 Builds vector DB using ChromaDB.
- 🧠 Generates new questions via LLMs with LangChain & Ollama.
- 💻 Interactive Gradio UI for UPSC aspirants and educators.
- ⚙️ Modular codebase and structured folders.

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

### 1. Install Python dependencies

pip install -r requirements.txt

### 2. Install and Run Ollama

    Download and install from: https://ollama.com

    Start the Ollama server: ollama serve

    Pull a model (e.g., phi3, mistral, etc.): ollama pull phi3

Optional: Link models from another disk

export OLLAMA_MODELS="/path/to/external/drive/ollama/models"

You can add that to .bashrc or .zshrc for persistence.

## 🧪 How to Run

➤ Step 1: Parse UPSC PDFs

Place your GS question paper PDFs into pyq_data/. Then run:

python parse_papers.py

➤ Step 2: Tag Questions

python tag_questions.py

➤ Step 3: Build Vector Store

python vector_store.py

➤ Step 4: Generate New Questions

python generate_questions.py

➤ Step 5: Run UI

python app.py

Then open the link shown in the terminal to access the Gradio interface.
📚 Tech Stack
Tool	Use
Python	Core programming
PyMuPDF	Extract questions from PDFs
LangChain	Prompt chaining
Ollama	Run local LLMs (phi3, etc.)
ChromaDB	Vector DB
Gradio	User interface
Supabase	(Optional) Cloud sync

## 🧠 Use Cases

    Generate mock UPSC GS questions

    Practice for prelims/mains with AI-curated content

    Academic content generation for coaching institutes

## 🛠️ To-Do

Filter by topic (e.g., Polity, IR, Geography)

Save generated sets as PDFs

Add answer key generation (GPT-style reasoning)

    Supabase backend for cloud storage

## 🧑‍💻 Author
Hardhik M

## 🪪 License
This project is licensed under the MIT License.

🌟 Star this repo if you find it helpful!
