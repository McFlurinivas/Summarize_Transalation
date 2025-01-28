# Whisper-Powered Audio Transcription with Summarization and Translation Using RAG

This project demonstrates the usage of a Retrieval-Augmented Generation (RAG) model, combining multiple tools like Whisper for transcription, Ollama for language models, and Langchain for document processing. The project extracts audio from files, transcribes it to text, and processes the transcription using advanced NLP pipelines for translation and summarization.

This project implements a Retrieval-Augmented Generation (RAG) model using the LangChain framework. It uses the following components:
- **Ollama Client**: To interact with the LLM (e.g., `llama3.1`).
- **Whisper**: To transcribe audio files into text.
- **LangID**: To detect the language of the transcribed text.
- **HuggingFaceEmbeddings**: To generate vector embeddings for document storage and retrieval.
- **LangChain Utilities**: For text splitting, embedding, and managing the RAG workflow.

## Features
1. **Audio Transcription**: Uses Whisper to transcribe audio files into text.
2. **Language Detection**: Automatically detects the language of the transcribed text.
3. **Text Splitting**: Splits text into smaller chunks for efficient processing.
4. **Vector Store Management**: Stores documents as embeddings using HuggingFace for retrieval.
5. **Translation and Summarization**: Translates the text into a target language and generates a summary.

## Code Workflow

This README outlines the workflow of the script, detailing the processes involved in transcription, language detection, document processing, translation, summarization, and error handling.

1. **Transcription**: Audio files are processed using Whisper to extract text.
2. **Language Detection**: The `langid` library is used to identify the language of the transcribed text.
3. **Document Processing**: The text is split into chunks using `RecursiveCharacterTextSplitter`. Vector embeddings are generated using HuggingFace models.
4. **Translation and Summarization**: The `ChatPromptTemplate` handles translation and summarization prompts. The Ollama client processes the prompts and generates outputs.

## Prerequisites
- Ollama Client
- Whisper Base version
- Python 3.8+
- Install the required dependencies from the `requirements.txt` file.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/McFlurinivas/Whisper-Powered-Audio-Transcription-with-Summarization-and-Translation-Using-RAG.git

2. Install dependencies:
   ```bash
   pip install -r requirements.txt

3. Download the Whisper model if it is not already cached:
   ```bash
   pip install git+https://github.com/openai/whisper.git

## How To Run:
1. Prepare an Audio File:
- Ensure the audio file is in one of the supported formats: `.mp3`, `.wav`, `.m4a`.
- Place the file in the project directory (e.g., `french.mp3`).

2. Follow Prompts
- The script will prompt you to enter a target language for translation.

3. Outputs
- The transcription of the audio file will be saved to transcription.txt.
- The detected language of the transcription will be printed.
- The extracted text and its translation will be displayed.
- A summary of the translated text will also be shown.

## Notes

- Ensure the audio file is clear for accurate transcription.
- Whisper may take longer to process large audio files.
- The HuggingFace model and Ollama client require sufficient system resources to run efficiently.

## Acknowledgements
This project utilizes:
- Ollama Client
- LangChain Framework
- Whisper
- HuggingFace Transformers
