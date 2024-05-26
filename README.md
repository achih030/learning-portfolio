# Learning Portfolio Summarizer

## Overview
The Learning Portfolio Summarizer is a tool designed to extract text from images and generate a summary of learning experiences based on that text. It utilizes the Google Cloud Vision API for text extraction and OpenAI's GPT-3.5 model for summarization.

## Features
- Extracts text from image files (PNG, JPG, JPEG).
- Summarizes learning experiences based on extracted text.
- Supports generating summaries in Chinese language.

## Installation
1. Clone this repository to your local machine.
2. Install the required dependencies:
    ```bash
    !pip install openai==0.28
    !pip install google-cloud-vision
    ```
3. Set up API keys for Google Cloud Vision and OpenAI. Replace `google-cloud.json` with your Google Cloud Vision service account key and `open_api_key` with your OpenAI API key in the file.

## Usage
1. Run the script.
2. Follow the prompts to upload image files containing text.
3. Enter the time, process, and your feelings.
4. The tool will extract text from the images and generate a summary of learning experiences.
5. The summary will be displayed in the console.

## APIs Used
- **Google Cloud Vision API**: Used for text extraction from image files. This API provides powerful optical character recognition (OCR) capabilities, enabling the extraction of text content from images with high accuracy.
- **OpenAI API (GPT-3.5)**: Utilized for text summarization. OpenAI's GPT-3.5 model is a state-of-the-art natural language processing model capable of generating human-like text responses. It powers the summarization component of the Learning Portfolio Summarizer, allowing it to produce coherent and contextually relevant summaries of learning experiences.
