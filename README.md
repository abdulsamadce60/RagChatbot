This project is a local AI-powered chatbot that lets you ask natural language questions about a pizza restaurant and get answers grounded in real customer reviews.
It uses a Retrieval-Augmented Generation (RAG) architecture: restaurant reviews from a CSV file are converted into vector embeddings using the mxbai-embed-large model via Ollama and stored in a persistent ChromaDB vector store. When a user asks a question, the most semantically relevant reviews are retrieved from the database and passed — along with the question — into a locally running llama2 model, which generates a contextual, informed response.
Tech stack: Python · LangChain · Ollama · ChromaDB · Pandas
Key features:

Fully local — no external API keys required
Persistent vector store (built once, reused across sessions)
Semantic search over reviews, not just keyword matching
Interactive CLI chat loop
