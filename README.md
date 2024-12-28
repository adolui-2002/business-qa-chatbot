# RAG-Based Chatbot with LangChain, ChatGPT, Pinecone, and Streamlit

## Overview
The Business QA Chatbot is an intelligent question-answering system designed to provide accurate and relevant answers to business-related queries. It is a Retrieval-Augmented Generation (RAG) chatbot that uses OpenAI's GPT-4, LangChain, Pinecone, and Streamlit to deliver a seamless and interactive experience.

## Features
- **Natural Language Processing**: Understands and processes user queries in natural language.
- **Contextual Responses**: Provides accurate answers based on the context of the conversation.
- **Memory Integration**: Maintains conversation context using LangChain's buffer memory.
- **Interactive Interface**: User-friendly interface built with Streamlit.
- **Scalable**: Uses Pinecone for efficient and scalable vector search.

## Project Structure
```plaintext
business-qa-chatbot/
├── Openai_Pinecone_Indexing_.ipynb  # Jupyter Notebook for indexing documents
├── app.py                           # Main application file
├── utils.py                         # Utility functions for the chatbot
├── requirements.txt                 # Python dependencies
└── README.md                        # Project documentation
```

## Tech Stack
- **Backend**: Python, LangChain, OpenAI GPT-4
- **Vector Database**: Pinecone
- **Web Framework**: Streamlit
- **Embedding Model**: text-embedding-ada-002 (via SentenceTransformers)
- **Other Tools**: Streamlit Chat, OpenAI API

  
## Getting Started

### Prerequisites
- Python 3.8 or higher
- An OpenAI API key
- A Pinecone API key

### Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/adolui-2002/business-qa-chatbot.git
    cd business-qa-chatbot
    ```

2. Create a virtual environment and activate it:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

4. Set up environment variables:
    - Create a `.env` file in the root directory with the following content:
      ```env
      OPENAI_API_KEY=your_openai_api_key
      PINECONE_API_KEY=your_pinecone_api_key
      ```

### Running the Application
1. Start the Streamlit application:
    ```sh
    streamlit run app.py
    ```

2. Open your web browser and navigate to `http://localhost:8501` to interact with the chatbot.

## Usage
- Enter your query in the input box and press Enter.
- The chatbot will process your query and provide a relevant response based on the indexed documents.

## Customization
### Indexing New Documents
- To index new documents, modify the `Openai_Pinecone_Indexing_.ipynb` notebook:
  - Update the `directory` variable to point to your document directory.
  - Run the notebook to index the new documents.

### Refining Queries
- The `utils.py` file contains functions for refining queries and finding matches. You can customize these functions to improve the chatbot's performance based on your specific use case.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- [OpenAI](https://openai.com) for providing the GPT-4 model.
- [Pinecone](https://www.pinecone.io) for the vector database service.
- [Streamlit](https://streamlit.io) for the interactive web framework.
- [LangChain](https://langchain.com) for providing tools to build language model-powered applications.

