# Stock Price Analyzer using LangChain and Streamlit

## Overview

This project implements a Stock Price Analyzer tool that allows users to input news article URLs and retrieve relevant information using OpenAI's language model. The application processes the content of the provided URLs, extracts relevant data, and enables users to ask questions about the news articles. The results, including answers and sources, are displayed in a user-friendly interface built with Streamlit.

## Features

- **URL Input**: Users can input up to three news article URLs for analysis.
- **Data Processing**: The application loads and processes the content of the provided URLs.
- **Text Splitting**: The content is split into smaller, manageable documents for better analysis.
- **Embedding and Indexing**: Utilizes OpenAI embeddings to create a FAISS index for efficient retrieval of information.
- **Question-Answering**: Users can ask questions related to the news articles, and the application retrieves answers along with their sources.
- **User -Friendly Interface**: Built with Streamlit for an interactive and responsive user experience.

## Requirements

- Python 3.x
- Streamlit
- LangChain
- OpenAI
- FAISS
- python-dotenv

You can install the required packages using pip:

```bash
pip install streamlit langchain openai faiss-cpu python-dotenv
```

## Usage

1. **Environment Setup**: Create a `.env` file in the project directory and add your OpenAI API key:

   ```
   OPENAI_API_KEY=your_openai_api_key
   ```

2. **Run the Application**: Execute the Streamlit application using the following command:

   ```bash
   streamlit run stock_price_analyzer.py
   ```

3. **Input URLs**: In the sidebar, enter up to three news article URLs that you want to analyze.

4. **Process URLs**: Click the "Process URLs" button to load and process the content of the entered URLs.

5. **Ask Questions**: After processing, enter your questions in the provided input field to retrieve answers based on the news articles.

6. **View Results**: The application will display the answers along with the sources from which the information was derived.

## Code Explanation

- **URL Loading**: The `UnstructuredURLLoader` is used to load content from the specified URLs.
- **Text Splitting**: The `RecursiveCharacterTextSplitter` splits the loaded text into smaller chunks for better processing.
- **Embedding Creation**: OpenAI embeddings are generated from the documents, and a FAISS index is created for efficient retrieval.
- **Question-Answering Chain**: The `RetrievalQAWithSourcesChain` is used to process user queries and retrieve relevant answers and sources.

## Example Output

The output will display the answer to the user's question along with the sources from which the information was derived, providing a comprehensive overview of the news articles.

## Contributing

Contributions are welcome! If you have suggestions for improvements or additional features, feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

---

Feel free to modify the README as needed to better fit your project's specifics or to add any additional information that may be relevant!
