[![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-blue?logo=kaggle)](https://www.kaggle.com/code/yourusername/gemini-rag-system)


# Gemini RAG System Notebook

This repository contains a notebook-based Retrieval-Augmented Generation (RAG) demo that uses **Google Gemini** and **PDF context extraction**.

# Gemini RAG System Notebook

🔗 **Live Kaggle Notebook:**  
[NoteBook](https://www.kaggle.com/code/veertiiiiwari/gemini-rag-system)

## What the notebook does

The notebook follows a simple end-to-end RAG flow:

1. Installs required Python packages (`google-generativeai`, `PyPDF2`).
2. Loads your Gemini API key from Kaggle Secrets (`GEMINI_API_KEY`).
3. Initializes the Gemini model (`gemini-2.5-flash`).
4. Extracts text from a PDF file.
5. Builds a prompt that forces answers to come only from the provided document.
6. Runs a sample question against the extracted PDF content.

## Requirements

- A Kaggle notebook/runtime environment.
- A configured Kaggle secret named `GEMINI_API_KEY`.
- Access to the target PDF file in your Kaggle input dataset.

## How to run

1. Open the notebook file (`gemini-rag-system` / `gemini-rag-system.ipynb`) in Kaggle or Jupyter.
2. Make sure your `GEMINI_API_KEY` is set in Kaggle Secrets.
3. Update the PDF path in cell 3 if needed:

   ```python
   pdf_path = "/kaggle/input/datasets/veertiiiiwari/eng-pdf/lefl101.pdf"
   ```

4. Run all cells in order.
5. Edit the `question` variable in cell 5 to ask your own questions.

## Customization ideas

- Replace the PDF source with your own documents.
- Add text chunking + embeddings for larger documents.
- Store chunks in a vector database for scalable retrieval.
- Add citation snippets in answers.

## Current limitations

- Uses full-document prompting (no chunked retrieval), which may not scale for very large PDFs.
- Designed for Kaggle Secrets usage (`kaggle_secrets` import).
- Prompt-based grounding only (no strict citation verification).

