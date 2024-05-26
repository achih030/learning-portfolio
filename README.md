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
3. Set up API keys for Google Cloud Vision and OpenAI. Replace `google_cloud.json` with your Google Cloud Vision service account key and `open_api_key` with your OpenAI API key in the `main.py` file.

## Usage
1. Run the script `main.py`.
2. Follow the prompts to upload image files containing text.
3. The tool will extract text from the images and generate a summary of learning experiences.
4. The summary will be displayed in the console.

## Contributing
Contributions are welcome! If you have any ideas for improvements or find any issues, feel free to open an issue or submit a pull request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
