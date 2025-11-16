# Basic LangChain Agent with RAG

Jupyter Notebook for creating basic agent and presenting how it can work. 
- Agent is able to retrieve text from mortgage technical docummentation.
- RAG is provided as LangChain tool to make use it only when needed and run better RAG querries

## Project Structure
```
project/
├── documents/
│   ├── slownik_pojec.pdf
│   ├── ustawa.pdf
├── notebooks/
│   └── agent_rag_as_tool.ipynb
├── requirements.txt
├── README.md
├── .env
└── .gitignore

```

## Setup & Installation

### 1. Clone/Download the project
```bash
git clone https://github.com/KrystianLata/langchain-rag-agent.git
cd langchain-rag-agent
```

### 2. Create virtual environment
```bash
# Create venv
python -m venv venv

# Activate (Windows)
venv\Scripts\activate

# Activate (Mac/Linux)
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Provide OPENAI_API_KEY 
Open file .env and replace OPENAI_API_KEY value with your actual key

### 5. Launch Jupyter Notebook
```bash
jupyter notebook
```
Then open `notebooks/agent_rag_as_tool.ipynb` and select venv as kernel

## 6. Data / documentation
The uploaded documents contains:
- **slownik_pojec.pdf** - generated dictionary of terms related to the morgage context
- **ustawa.pdf** - law document about mortgage

## 7. Features of created pipeline:
1. Document Processing - Load and chunk PDF documents using LangChain
2. Vector Search - Create embeddings and semantic search with ChromaDB
3. RAG Implementation - Build Retrieval-Augmented Generation pipeline
4. 2 Versions of LLM with RAG implementation:
    - Chatbot "always-on RAG" 
    - Agent with RAG tool (agent decides when RAG is needed)
