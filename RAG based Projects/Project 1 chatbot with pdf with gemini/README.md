This code implements a simple Retrieval-Augmented Generation (RAG) chatbot using Streamlit, LangChain, and Gemini Pro. Here’s a breakdown of what each part does:

Imports & Setup

Loads required libraries for Streamlit UI, PDF loading, text splitting, embeddings, vector storage, LLM, and prompt templates.
Loads environment variables (for API keys, etc.) using dotenv.
Streamlit UI

Sets the app title: "RAG Application using Gemini Pro".
Document Loading & Processing

Loads a PDF file (my_paper.pdf) using PyPDFLoader.
Splits the PDF into manageable text chunks (size 1000 characters) for processing.
Vector Store & Retriever

Embeds the document chunks using Google’s embedding model.
Stores embeddings in a Chroma vector database.
Sets up a retriever to fetch the top 10 most similar chunks for any query.
LLM Setup

Initializes Gemini Pro as the language model.
Prompt & Chain Construction

Waits for user input via a chat box.
Defines a system prompt instructing the LLM to answer using retrieved context, concisely.
Builds a prompt template for the LLM.
If the user submits a query:
Creates a chain that retrieves relevant context and generates an answer.
Invokes the chain with the user’s input.
Prints and displays the answer in the Streamlit app.
Summary:
The app lets users ask questions about the content of a PDF. It retrieves relevant sections from the PDF, feeds them to Gemini Pro, and returns concise answers.


Step 1: Created Virtual env for main folder usng conda create -n gitprojects python=3.12

step 2 : to clear terminal zsh : command is zsh

step 3: Get gemini api key 

