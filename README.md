# Hybrid Search System

## Overview

Hybrid Search System is an advanced search application that combines dense vector search, sparse keyword search, and reranking techniques to improve search relevance and retrieval accuracy.

The system integrates multiple search technologies, including FAISS, Elasticsearch, and Whoosh, and uses Hugging Face reranking models to return the most relevant results to user queries.

## Features

* Dense vector search using FAISS
* Full-text search using Elasticsearch
* Keyword-based search using Whoosh
* Hybrid retrieval combining dense and sparse search results
* Semantic search using embeddings
* Result reranking using Hugging Face Cross-Encoder models
* Fast and scalable document retrieval
* Support for custom document indexing

## Architecture

```text
User Query
     │
     ▼
Query Processing
     │
     ├──► FAISS Vector Search
     │
     ├──► Elasticsearch Search
     │
     └──► Whoosh Search
                │
                ▼
      Result Aggregation
                │
                ▼
     Hugging Face Reranker
                │
                ▼
         Final Results
```

## Technology Stack

* Python
* FAISS
* Elasticsearch
* Whoosh
* Hugging Face Transformers
* Sentence Transformers
* NumPy
* Pandas

## Project Structure

```text
Hybrid_Search/
│
├── data/
├── indexes/
├── notebooks/
├── models/
├── src/
├── requirements.txt
├── .env
└── README.md
```

## Installation

### Clone the Repository

```bash
git clone <repository_url>
cd Hybrid_Search
```

### Create Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

Windows:

```bash
venv\Scripts\activate
```

Linux/Mac:

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

## Configuration

Create a `.env` file and add the required configuration values:

```env
ELASTIC_HOST=your_elasticsearch_host
ELASTIC_USER=your_username
ELASTIC_PASS=your_password
```

## Usage

Run the application:

```bash
python main.py
```

Example Query:

```text
What is machine learning?
```

Example Output:

```text
1. Introduction to Machine Learning
2. Machine Learning Fundamentals
3. Applications of Artificial Intelligence
```

## Search Workflow

1. Convert documents into embeddings.
2. Index embeddings in FAISS.
3. Index documents in Elasticsearch and Whoosh.
4. Execute dense and sparse searches for each query.
5. Merge retrieved results.
6. Rerank results using a Hugging Face Cross-Encoder model.
7. Return the highest-ranked documents.

## Use Cases

* Enterprise Search
* Knowledge Base Search
* Document Retrieval Systems
* Retrieval-Augmented Generation (RAG)
* Internal Search Applications

## Future Enhancements

* Query Expansion
* Multi-language Search Support
* Learning-to-Rank Models
* Streamlit Web Interface
* LLM-based Answer Generation
* Distributed Search Infrastructure

## Author

Pooja Thorat
