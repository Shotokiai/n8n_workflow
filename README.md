# PDF Reader Chatbot (n8n workflow)

This repository contains the workflow for a PDF Reader Chatbot built using n8n, OpenAI, Pinecone, and Google Drive. The workflow enables users to upload PDF files to a Google Drive folder, automatically ingest the content into a vector database (Pinecone), and interact with the content using a conversational AI agent powered by OpenAI.

## Features
- **Automated PDF ingestion**: Monitors a Google Drive folder for new PDF uploads and processes them automatically.
- **Vector database integration**: Uses Pinecone to store and retrieve document embeddings for efficient semantic search.
- **Conversational AI**: Utilizes OpenAI's GPT models to answer user questions based on the ingested PDF content.
- **Memory and context**: Maintains conversational context for more natural interactions.
- **Strict tool usage**: The AI agent always uses the vector store for answering questions, ensuring responses are grounded in the uploaded documents.

## Tech Stack
- **n8n**: Workflow automation platform
- **OpenAI**: Language model for conversational AI and embeddings
- **Pinecone**: Vector database for semantic search
- **Google Drive**: Cloud storage for PDF uploads

## How it works
1. **File Upload**: User uploads a PDF to a specific Google Drive folder.
2. **Trigger**: n8n detects the new file and downloads it.
3. **Embedding & Storage**: The PDF is processed, embeddings are generated using OpenAI, and stored in Pinecone.
4. **Chatbot Interaction**: Users interact with the chatbot, which retrieves relevant information from Pinecone and answers using OpenAI.

## Setup
- Configure Google Drive, OpenAI, and Pinecone credentials in n8n.
- Import the provided workflow JSON into your n8n instance.
- Set up the required Google Drive folder and Pinecone index.

## License
This project is for educational and demonstration purposes.
