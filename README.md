# Audiovision – AI That Reads Images Aloud

> An AI-powered tool that takes an image as input, understands its content using a Large Language Model (LLM), and converts the generated description into natural-sounding speech.

---

## 📌 Overview

This project combines the power of **vision-language models** and **text-to-speech (TTS)** synthesis to make images accessible and interactive. Upload any image, and the tool will:

1. **Analyze** the image using an LLM (e.g., GPT-4 Vision / Claude / Gemini)
2. **Generate** a natural language description of the image
3. **Convert** that description into spoken audio output

This is particularly useful for **accessibility tools**, **visually impaired users**, **content automation**, and **educational applications**.

---

## ✨ Features

- 📷 Accepts images from local file upload or URL
- 🤖 Uses a multimodal LLM to understand and describe image content
- 🗣️ Converts generated text to speech using a TTS engine
- 🌐 Simple and intuitive interface
- ⚡ Fast and lightweight pipeline

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| Language | Python |
| LLM | OpenAI GPT-4 Vision / Anthropic Claude / Google Gemini |
| Text-to-Speech | OpenAI TTS / gTTS / pyttsx3 |
| UI (optional) | Streamlit / Gradio |
| Image Handling | Pillow (PIL) |

---

## 📁 Project Structure

```
Image-to-Speech-GenAI-Tool/
│
├── app.py                  # Main application entry point
├── image_to_text.py        # LLM image description module
├── text_to_speech.py       # TTS conversion module
├── utils.py                # Helper utilities
├── requirements.txt        # Python dependencies
├── .env.example            # Environment variables template
└── README.md               # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- An API key for your chosen LLM provider (OpenAI / Anthropic / Google)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/Image-to-Speech-GenAI-Tool.git
   cd Image-to-Speech-GenAI-Tool
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env and add your API keys
   ```

   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   # or
   ANTHROPIC_API_KEY=your_anthropic_api_key_here
   ```

### Running the App

```bash
python app.py
```

Or if using Streamlit:

```bash
streamlit run app.py
```

---

## 🧪 Usage

1. Launch the application
2. Upload an image (JPG, PNG, WEBP) or provide an image URL
3. Click **"Generate Speech"**
4. The tool will display the generated description and play the audio

### Example

```python
from image_to_text import describe_image
from text_to_speech import speak

description = describe_image("path/to/image.jpg")
speak(description)
```

---

## 📦 Requirements

```
openai
anthropic
pillow
gtts
requests
python-dotenv
streamlit      # optional, for UI
```

Install all at once:
```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

| Variable | Description |
|----------|-------------|
| `OPENAI_API_KEY` | Your OpenAI API key |
| `ANTHROPIC_API_KEY` | Your Anthropic Claude API key |
| `GOOGLE_API_KEY` | Your Google Gemini API key |

---

## 🙏 Acknowledgements

- [OpenAI](https://openai.com/) for GPT-4 Vision and TTS APIs
- [Anthropic](https://www.anthropic.com/) for Claude Vision
- [gTTS](https://gtts.readthedocs.io/) for text-to-speech support
- [Streamlit](https://streamlit.io/) / [Gradio](https://gradio.app/) for the UI framework

---

> Built with ❤️ using Generative AI
