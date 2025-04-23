
# Local AI Agent with DeepSeek 14B

This project runs a local AI assistant powered by the DeepSeek 14B model using LangChain and Ollama. The assistant answers questions about a pizza restaurant based on review data.

## Features

- Uses DeepSeek 14B via Ollama
- Retrieves relevant reviews using vector search
- Runs fully locally, no external API calls

## Requirements

- Python 3.9+
- Ollama installed and running (`ollama run deepseek-r1:14b`)
- CSV file: `realistic_restaurant_reviews.csv`

## Setup

1. Clone this repo and navigate to the directory.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Ensure Ollama is running with the required models:
   - `deepseek-r1:14b` (for chat)
   - `nomic-embed-text` (for embeddings)

## Running

```bash
python main.py
```

You can then type your questions in the terminal. To quit, enter `q`.

## Notes

- Review data is loaded from `realistic_restaurant_reviews.csv`
- First run will build a local vector store using Chroma

## File Overview

- `main.py`: Loads the LLM and handles user interaction
- `vector.py`: Loads review data and sets up vector retrieval
