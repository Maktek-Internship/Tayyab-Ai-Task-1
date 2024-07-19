Chat With Websites
This application allows users to interact with multiple websites by asking questions and retrieving answers based on the content of those websites. The app uses a combination of web crawling, document embedding, and conversational AI to provide responses.

Features
Web Crawling: Extracts content from the provided URLs.
Document Embedding: Uses Google Generative AI embeddings to create vector representations of the documents.
Conversational AI: Utilizes the Llama3-70b model for generating responses to user queries.
Streamlit Interface: Provides an interactive web interface for users to input URLs and ask questions.
Requirements
Python 3.8 or higher
Streamlit
LangChain
GoogleGenerativeAIEmbeddings
FireCrawlLoader
Chroma
ChatGroq
dotenv
selenium
twocaptcha
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/chat-with-websites.git
cd chat-with-websites
Create and activate a virtual environment:

bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install the required packages:

bash
Copy code
pip install -r requirements.txt
Set up environment variables by creating a .env file in the project root and adding your keys:

env
Copy code
APIKEY_2CAPTCHA=your-2captcha-api-key
Usage
Run the Streamlit app:

bash
Copy code
streamlit run app.py
Open your browser and navigate to the local URL provided by Streamlit.

Enter the URLs of the websites you want to crawl and process in the sidebar. Click "Submit URLs" to start the processing.

Once the URLs are processed, you can ask questions in the main area, and the app will provide answers based on the content of the websites.

Code Overview
app.py
This is the main script that runs the Streamlit application. It includes functions for:

Loading and processing URLs
Embedding documents
Querying the embedded data
Displaying the Streamlit interface
Key Functions
bypass_captcha(url): Handles CAPTCHA bypassing using the 2Captcha service.
process_urls(urls): Processes the provided URLs, crawls the content, and embeds the documents.
process_query(vectordb, query, chat_history): Handles user queries and retrieves answers from the embedded documents.
main(): Sets up the Streamlit interface and handles user interactions.
Notes
CAPTCHA bypassing requires a 2Captcha API key. Make sure to provide a valid key in your .env file.
The app uses the Llama3-70b model for generating responses. Adjust the model parameters as needed for your use case.
