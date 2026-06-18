# RAG Model

This repository contains a notebook-first retrieval-augmented generation (RAG) prototype for ingesting PDF documents, preparing them for embedding, and storing the processed content in a vector database.

The main implementation currently lives in [notebook/rag_pipeline.ipynb](notebook/rag_pipeline.ipynb). The notebook focuses on:

- loading PDF files from a local folder
- extracting document text with LangChain loaders
- attaching source metadata to each document
- preparing the documents for chunking, embeddings, and vector storage

## Project Structure

- [main.py](main.py) - minimal Python entry point for the package scaffold
- [notebook/rag_pipeline.ipynb](notebook/rag_pipeline.ipynb) - the RAG ingestion pipeline notebook
- [notebook/document.ipynb](notebook/document.ipynb) - supporting notebook
- [data/datafiles](data/datafiles) - sample PDF documents used by the pipeline
- [pyproject.toml](pyproject.toml) - project metadata and dependencies

## Requirements

- Python 3.13 or newer
- A Jupyter-capable editor or environment

Python dependencies currently listed in the project:

- ipykernel
- langchain
- langchain-community
- langchain-core
- pymupdf
- pypdf
- uv

## Setup

1. Create or activate a Python environment.
2. Install the project dependencies.

If you are using uv, the project can be installed with:

```bash
uv sync
```

If you prefer pip, install the packages from the project configuration or your own requirements workflow.

## Usage

1. Open [notebook/rag_pipeline.ipynb](notebook/rag_pipeline.ipynb).
2. Point the notebook at a folder of PDFs, such as [data/datafiles](data/datafiles).
3. Run the ingestion cells to load documents and add metadata.
4. Continue with your splitting, embedding, and vector database steps in the notebook.

## Notes

- The current main.py file is only a placeholder and does not yet run the RAG pipeline.
- The repository appears to be in an early development stage, so the notebook is the authoritative source for the pipeline logic.
