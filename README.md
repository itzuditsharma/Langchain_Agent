# AI Agent with Wikipedia and Arxiv Tools

This repository contains an implementation of an AI agent that leverages Wikipedia and Arxiv tools for retrieving and processing information. The notebook uses LangChain utilities to interact with these data sources efficiently.

## Features
- **Wikipedia Query Tool**: Fetches information from Wikipedia using LangChain.
- **Arxiv Tool**: Retrieves research papers from Arxiv.
- **OpenAI API Integration**: Uses OpenAI API for enhanced data processing.
- **Environment Variables Support**: Loads API keys from environment variables securely.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/itzuditsharma/Langchain_Agent.git
   cd Langchain_Agent
   ```
2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```
3. Set up environment variables:
   ```bash
   cp .env.example .env
   ```
   Fill in your OpenAI API key and other required credentials in the `.env` file.

## Usage

Run the notebook interactively:
```bash
jupyter notebook try_agents.ipynb
```

## Dependencies
- `langchain`
- `openai`
- `wikipedia-api`
- `arxiv`
- `dotenv`

Install dependencies using:
```bash
pip install -r requirements.txt
```

## Example Code
```python
from dotenv import load_dotenv
load_dotenv()
import os

os.environ["OPENAI_API_KEY"] = os.getenv("OPENAI_API_KEY")
from langchain_community.tools import WikipediaQueryRun
from langchain_community.utilities import WikipediaAPIWrapper
```

## Contributing
Feel free to fork this repository and submit pull requests with improvements.

## License
This project is licensed under the MIT License.

