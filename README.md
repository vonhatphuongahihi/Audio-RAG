# 🎵 Voice RAG - Chat with Audio Files 
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org) [![Streamlit](https://img.shields.io/badge/Streamlit-Web%20App-red.svg)](https://streamlit.io) [![LangChain](https://img.shields.io/badge/LangChain-RAG%20Framework-green.svg)](https://langchain.com) [![Ollama](https://img.shields.io/badge/Ollama-Local%20LLM-purple.svg)](https://ollama.ai)

A simple Voice RAG (Retrieval-Augmented Generation) system using Deepseek, LangChain, and Streamlit to chat with audio files and answer complex questions about them.

## Features

- **Audio Transcription**: Automatically transcribes uploaded audio files using OpenAI Whisper
- **Intelligent Q&A**: Ask questions about the audio content and get contextual answers
- **Vector Search**: Uses embeddings to find relevant parts of the transcribed text
- **Streamlit Interface**: Clean and intuitive web interface for easy interaction

## Pre-requisites

1. **Install Ollama** on your local machine from the [official website](https://ollama.ai/)

2. **Pull the Deepseek model**:
   ```bash
   ollama pull deepseek-r1:8b
   ```

3. **Install FFmpeg** (required for audio processing):
   - Download from [FFmpeg website](https://ffmpeg.org/download.html)
   - Add to your system PATH or place in `C:\ffmpeg\bin` (Windows)

## Installation

1. **Clone or download this repository**

2. **Install the dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Run the Streamlit app**:
   ```bash
   streamlit run voice_rag.py
   ```

2. **Upload an audio file**:
   - Supported formats: MP3, WAV
   - The audio will be automatically transcribed

3. **Ask questions**:
   - Type your questions in the chat interface
   - Get intelligent answers based on the audio content

## How it Works

1. **Audio Processing**: Uploaded audio files are transcribed using OpenAI Whisper
2. **Text Chunking**: The transcribed text is split into manageable chunks
3. **Vector Embedding**: Text chunks are converted to embeddings using Deepseek
4. **Retrieval**: When you ask a question, the system finds the most relevant text chunks
5. **Generation**: The LLM generates answers based on the retrieved context

