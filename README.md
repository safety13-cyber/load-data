# nami-bot2

![alt text](image-2.png)

## Overview
nami-bot2 is a Flask-based web application that allows users to chat with a bot. The bot is powered by OpenAI's GPT-3.5-turbo model and role-plays as Nami from One Piece.

## Features
- Chat with a bot that role-plays as Nami from One Piece.
- Simple and clean user interface.
- Powered by OpenAI's GPT-3.5-turbo model.

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/nami-bot2.git
    cd nami-bot2
    ```

2. Create a virtual environment and activate it:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

4. Set your OpenAI API key in .py[`GET.py`](GET ):
    ```python
    openai.api_key = 'your-openai-api-key'
    ```

## Usage
1. Run the Flask application:
    ```sh
    python GET.py
    ```

2. Open your web browser and go to `http://127.0.0.1:5000/`.

3. Type your message in the input box and click "Send" to chat with the bot.

## GitHub Actions Workflow
This project includes a GitHub Actions workflow to automate testing and deployment.

```mermaid
graph TD;
    A[Deploy Flask App] --> B[on: push to main branch]
    B --> C[build job]
    C --> D[Checkout code]
    C --> E[Set up Python 3.8]
    C --> F[Install dependencies]
    C --> G[Run tests]
    B --> H[deploy job]
    H --> I[Checkout code]
    H --> J[Set up Python 3.8]
    H --> K[Install dependencies]
    H --> L[Deploy to Heroku]
