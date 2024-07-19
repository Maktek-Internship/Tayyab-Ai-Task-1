# Chat With Websites

This application allows users to interact with multiple websites by asking questions and retrieving answers based on the content of those websites. The app uses a combination of web crawling, document embedding, and conversational AI to provide responses.

## Features

- **Web Crawling**: Extracts content from the provided URLs.
- **Document Embedding**: Uses Google Generative AI embeddings to create vector representations of the documents.
- **Conversational AI**: Utilizes the Llama3-70b model for generating responses to user queries.
- **Streamlit Interface**: Provides an interactive web interface for users to input URLs and ask questions.

## Requirements

- Python 3.8 or higher
- Streamlit
- LangChain
- GoogleGenerativeAIEmbeddings
- FireCrawlLoader
- Chroma
- ChatGroq
- dotenv
- selenium
- twocaptcha

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/chat-with-websites.git
   cd chat-with-websites
