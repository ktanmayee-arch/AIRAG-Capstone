# AIRAG-Capstone
RAG System
# Finance Assistant

A simple finance assistant built as a Python script that uses OpenAI's chat completion API.

## Overview

This project demonstrates a lightweight finance helper that accepts a question or prompt and returns a concise response from the OpenAI API.

## Files

- `hello_llm.py` - main Python script that reads a prompt from the command line and sends it to OpenAI.
- `.env` - environment file to store the `OPENAI_API_KEY`.

## Setup

1. Install dependencies:
   ```bash
   pip install python-dotenv openai
   ```

2. Create a `.env` file in the project folder with your OpenAI API key:
   ```env
   OPENAI_API_KEY=your_api_key_here
   ```

## Usage

Run the script from the project folder with a finance-related question:

```bash
python hello_llm.py "What is a good strategy for building an emergency fund?"
```

If no prompt is provided, the script defaults to `Say hello.`

## Notes

- Keep your API key secret and never commit it to version control.
- The script uses the `gpt-4o-mini` model and sets the system role to return concise answers.

## Future Improvements

- Add explicit finance-specific system prompts.
- Expand to handle budgeting, investment guidance, and expense analysis.
- Add validation and error handling for API failures.
