# Corrective RAG Agent

![Corrective RAG Agent Workflow](/diagram.png)

## Project Description

The Corrective RAG Agent is an advanced question-answering system that utilizes Retrieval-Augmented Generation (RAG) techniques with additional corrective measures to ensure high-quality, relevant answers.

### Tech Stack

- **Llama3** <img src="https://raw.githubusercontent.com/gilbarbara/logos/29e8719bf78915c7a82a26a6c203f53c4cb8fff2/logos/meta-icon.svg" alt="llama" width="20" height="20"/> <!-- Llama3 -->
- **Firecrawl** 🔥
- **Langchain** 🦜️🔗

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