# Corrective RAG Agent

![Corrective RAG Agent Workflow](/CORR_RAG.png)

## Project Description

The Corrective RAG Agent is an advanced question-answering system that utilizes Retrieval-Augmented Generation (RAG) techniques with additional corrective measures to ensure high-quality, relevant answers.

### Tech Stack

<p align="left">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> <!-- Python icon for Llama3 -->
  <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="firebase" width="40" height="40"/> <!-- Firebase icon for Firecrawl -->
  <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/> <!-- TensorFlow icon for Langchain -->
</p>

- **Llama3**: Advanced language model for natural language processing
- **Firecrawl**: Web crawling and data extraction tool
- **Langchain**: Framework for developing applications powered by language models

### Workflow

1. **Question Input**: The process begins with a user-provided question.

2. **Retrieve Documents**: The system retrieves relevant documents based on the input question.

3. **Grade Documents**: Retrieved documents are graded for relevance and quality.

4. **Relevance Check**: The system checks if any retrieved document is relevant to the question.
   - If Yes: Proceeds to generate an answer.
   - If No: Initiates a web search for additional information.

5. **Generate Answer**: Using the relevant documents or web search results, the system generates an answer.

6. **Hallucination Check**: The generated answer is checked for potential hallucinations or inaccuracies.
   - If No hallucinations detected: The answer is provided to the user.
   - If Yes (hallucinations detected): The system asks if the answer addresses the question.
     - If Yes: The final answer is provided.
     - If No: The system initiates a web search for more accurate information.

7. **Web Search**: When needed, the system performs a web search to gather additional, up-to-date information to supplement or correct the answer.

### Key Features

- Document retrieval and relevance grading
- Web search integration for enhanced information gathering
- Hallucination detection and correction mechanism
- Iterative answer improvement process

This Corrective RAG Agent aims to provide accurate, relevant, and hallucination-free answers by combining the strengths of retrieval-based systems with generative AI and web search capabilities.

## Setup and Usage

### Installation

To set up the Corrective RAG Agent, you need to:
1. Install Ollama using the [official download link](https://ollama.com/download) or using the homebrew command:

```bash
brew install ollama
```

2. Install the required packages. Run the following command:

```bash
pip install -U langchain-nomic langchain_community tiktoken langchainhub chromadb langchain langgraph tavily-python gpt4all firecrawl-py
```