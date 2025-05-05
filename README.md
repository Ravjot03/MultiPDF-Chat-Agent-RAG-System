# MultiPDF Chat Agent RAG-System

The Multi-PDF Chat Agent is a fully functional Retrieval-Augmented Generation (RAG) system built in Python and Streamlit that enables users to:

- Upload multiple PDF documents
- Ask natural language questions
- Receive answers grounded in the PDF content

It uses OpenAI's GPT-3.5-Turbo as the language model and FAISS as the vector database to implement a highly responsive and accurate question-answering system over unstructured data.

## Problem it is solving 
PDFs are rich sources of information but hard to query efficiently. This project allows users to interact with their documents as if talking to a smart assistant — instantly retrieving and summarizing the most relevant information.

Use cases:
1. Legal document review
2. Scientific paper Q&A
3. Business report understanding
4. Internal knowledge base search
5. RFP/documentation analysis


## Architecture



## How the RAG pipeline works
1. Input PDFs: Users drag and drop one or more PDF documents.
2. Text Extraction: Each PDF is parsed into raw text using PyPDF2.
3. Chunking: Text is split into manageable, overlapping segments using LangChain’s RecursiveCharacterTextSplitter.
4. Embedding: Text chunks are embedded
5. Vector Indexing: Chunks are stored in a FAISS index.
6. Semantic Search: On user query, FAISS retrieves the most similar chunks.
7. Answer Generation: The relevant context is passed to OpenAI's GPT-3.5-Turbo, which generates a grounded, accurate answer.
8. Output: The result is displayed in the Streamlit UI.

