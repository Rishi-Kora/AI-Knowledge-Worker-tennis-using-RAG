


# AI Knowledge Worker: Tennis Q&A with RAG

An interactive Jupyter Notebook that leverages Retrieval-Augmented Generation (RAG) to build a “knowledge worker” for tennis. Ask natural-language questions about players, matches, and stats, and get precise, sourced answers powered by OpenAI’s API and a custom vector store.

---

## Features

- **Natural-language Q&A**  
  Ask anything about tennis history, player bios, match results, statistics, and more.
- **Retrieval-Augmented Generation**  
  Combines dense retrieval (via FAISS) with a large language model to ground answers in real documents.
- **Modular & Extensible**  
  Swap in your own document set (PDFs, articles, CSVs) to cover different sports or domains.
- **Interactive Notebook**  
  Step through the entire pipeline: data ingestion, embedding, index building, querying, and answer generation.

---

## Repository Contents
```markdown


├── AI Knowledge Worker\_tennis.ipynb   # Core notebook
├── data/                              # Sample tennis data (PDFs, CSVs, text)
├── embeddings/                        # Precomputed embeddings (optional)
├── env.example                        # Example .env file for API keys
├── requirements.txt                   # Python dependencies
└── LICENSE                            # MIT License

````

---

## Installation

1. **Clone the repo**  
   ```bash
   git clone https://github.com/Rishi-Kora/AI-Knowledge-Worker-tennis-using-RAG.git
   cd AI-Knowledge-Worker-tennis-using-RAG


2. **Create a Python virtual environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate      # macOS/Linux
   venv\Scripts\activate         # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Configure API keys**

   * Copy `env.example` to `.env`
   * Add your OpenAI API key (and any other keys) to `.env`

---

## Usage

1. **Launch the Notebook**

   ```bash
   jupyter lab
   ```

2. **Run through the cells** in `AI Knowledge Worker_tennis.ipynb`:

   * Load and preprocess your tennis documents
   * Embed text with OpenAI embeddings
   * Build/restore a FAISS vector index
   * Pose natural-language queries
   * View grounded, sourced responses

3. **Customize**

   * Drop in your own documents under `data/`
   * Adjust chunk size, retrieval parameters, or the LLM model in the notebook

---

##  Configuration Options

Inside the notebook you can tweak:

* **`CHUNK_SIZE`**: Text split size for embedding
* **`TOP_K`**: Number of top documents retrieved per query
* **LLM model**: e.g. `gpt-3.5-turbo` vs. `gpt-4`
* **FAISS index path**: Persist or load prebuilt indices

---

##  Extending to Other Domains

1. Replace the tennis content in `data/` with PDFs, text, or CSVs from your domain.
2. Update any domain-specific preprocessing (e.g. metadata extraction).
3. Re-run the notebook’s ingestion and indexing steps.

---

##  Contributing

Contributions are welcome! Please open an issue or submit a pull request for:

* New features (e.g. support for other vector stores)
* Bug fixes or performance improvements
* Expanded sample data or tutorials

---

##  License

This project is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

*Happy querying!* 

```

Let me know if you’d like any sections added or adjusted!
```
