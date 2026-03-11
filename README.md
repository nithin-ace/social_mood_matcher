#Social Mood Matcher

AI Caption & Hashtag Generator for Social Media

Project Overview

Social Mood Matcher is an AI-powered web application that automatically generates social media captions and hashtags from uploaded images. The system analyzes the mood or sentiment of an image and produces engaging captions along with trending hashtags suitable for platforms such as Twitter, Instagram, and Facebook.

The project integrates computer vision and natural language processing techniques to simplify social media content creation.

Key Features

Image sentiment detection using AI

Automatic caption generation

Trending hashtag generation

Social media character limit management

Multiple caption styles

Support for different social media platforms

Optional Google Gemini AI integration for enhanced analysis

Interactive web interface using Streamlit

Technologies Used

Programming Language

Python

Framework

Streamlit

AI / Machine Learning

BLIP Vision-Language Model

HuggingFace Transformers

Sentiment Analysis Model

Google Gemini Vision API (optional)

Libraries

Streamlit

Transformers

Torch

Pillow

NumPy

OpenCV

EasyOCR

Google Generative AI

System Architecture

The system follows a modular architecture consisting of the following components:

User
  │
  ▼
Streamlit Interface (app.py)
  │
  ├── Image Processing (image_utils)
  │
  ├── Sentiment Detection (image_sentiment)
  │
  ├── Caption Generator (caption_generator)
  │
  ├── Hashtag Engine (hashtag_engine)
  │
  └── Character Limiter (character_limiter)
Project Structure
Social-Mood-Matcher
│
├── app.py
│
├── services
│   ├── caption_generator.py
│   ├── character_limiter.py
│   ├── gemini_service.py
│   ├── hashtag_engine.py
│   └── image_sentiment.py
│
├── utils
│   ├── image_utils.py
│   └── text_utils.py
│
├── config
│   └── settings.py
│
├── models_cache
│
├── requirements.txt
│
└── README.md
Installation
1. Clone the Repository
git clone https://github.com/yourusername/social-mood-matcher.git
2. Navigate to the Project Folder
cd social-mood-matcher
3. Install Dependencies
pip install -r requirements.txt

If using manual installation:

pip install streamlit opencv-python easyocr pillow numpy google-generativeai transformers torch torchvision
Running the Application

Start the Streamlit application using the following command:

python -m streamlit run app.py

After running the command, open the browser at:

http://localhost:8501
How the System Works

User uploads an image.

The system validates and processes the image.

A BLIP model generates a caption describing the image.

Sentiment analysis determines the mood of the image.

Caption templates generate social media captions.

Trending hashtags are selected based on sentiment and category.

The character limiter ensures captions meet platform limits.

The final caption and hashtags are displayed to the user.

Example Output

Detected Sentiment

Happy (Confidence: 0.87)

Generated Caption

Living my best life! ✨

Generated Hashtags

#travel #nature #explore #wanderlust #happyvibes
Supported Platforms

The system supports caption generation optimized for:

Twitter (280 characters)

Instagram

Facebook

Optional Gemini AI Integration

Google Gemini Vision API can be used to improve image understanding and caption generation.

To enable this feature:

Obtain a Gemini API key.

Add the key to a .env file.

Example:

GEMINI_API_KEY=your_api_key_here
Future Improvements

Real-time trending hashtag detection

Multi-language caption generation

Image aesthetic scoring

Mobile application version

Social media auto-post integration
