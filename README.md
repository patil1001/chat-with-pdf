Conversational PDF Analyzer
This repository contains a Python-based application that allows users to interact with a PDF document using natural language queries. The application utilizes advanced language models and vector stores to provide accurate and relevant responses to user questions based on the content of the uploaded PDF file.

Features
PDF Processing: Upload and process PDF files to extract text content.
Conversational Retrieval: Engage in a conversation with the application to retrieve information from the PDF.
Advanced Language Models: Utilizes the power of GPT-4 and other advanced language models for generating responses.
Source Referencing: Provides references to the source documents from which the answers are derived.
Technologies Used
Python: The primary programming language for the application.
Langchain: For handling text splitting, vector stores, and conversational chains.
Chroma: Vector store used for efficient retrieval.
Chainlit: Framework for building conversational applications.
PyPDF2: Library for reading and extracting text from PDF files.
Environment Variables: Managed using dotenv for secure configuration.
Installation
Clone the Repository:

bash
Copy code
git clone https://github.com/yourusername/conversational-pdf-analyzer.git
cd conversational-pdf-analyzer
Create and Activate Virtual Environment:

bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install Dependencies:

bash
Copy code
pip install -r requirements.txt
Set Up Environment Variables:
Create a .env file in the root directory and add your API keys and other configurations.

env
Copy code
# Example .env file
GROQ_API_KEY=your_groq_api_key
Usage
Run the Application:

bash
Copy code
python app.py
Upload a PDF File:

On starting the application, you will be prompted to upload a PDF file. The application supports files up to 100 MB in size.
Ask Questions:

Once the PDF is processed, you can start asking questions about the content of the document. The application will provide answers along with references to the relevant sections of the PDF.
Code Overview
app.py
The main script that runs the application.

Imports:

Libraries for PDF processing, language models, and Chainlit are imported.
Language Models:

ChatOpenAI is configured to use GPT-4 with specific parameters.
Chat Start Event:

The on_chat_start function waits for a PDF file to be uploaded.
The PDF is read and its text content is extracted and split into manageable chunks.
A vector store is created using the extracted text.
A conversational retrieval chain is set up for handling user queries.
Message Handling:

The main function handles incoming messages.
It retrieves the conversational chain and processes the user's query.
The response is generated and sent back to the user, along with references to the source documents.
Contributing
Fork the Repository
Create a Feature Branch
bash
Copy code
git checkout -b feature/your-feature-name
Commit Your Changes
bash
Copy code
git commit -m 'Add some feature'
Push to the Branch
bash
Copy code
git push origin feature/your-feature-name
Open a Pull Request
License
This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgements
Special thanks to the developers of the Langchain, Chainlit, and PyPDF2 libraries for making this project possible.
