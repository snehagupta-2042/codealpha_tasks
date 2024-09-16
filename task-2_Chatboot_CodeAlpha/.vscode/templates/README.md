# CodeAlpha-Task-1-Chatbot-For-FAQs
 
## Overview

**MindCare Chatbot** is a conversational AI application designed to answer frequently asked questions about mental health. It leverages Natural Language Processing (NLP) techniques to understand and respond to user queries accurately, providing accessible mental health information.

## Features

- **Conversational Interface**: Designed to mimic the intuitive and user-friendly ChatGPT interface.
- **Advanced NLP Techniques**: Utilizes machine learning models to understand and respond to user queries.
- **Robust Backend**: Built with a Flask backend to handle POST requests and deliver responses efficiently.
- **Engaging Design**: Bold text for responses, improved color schemes, and user-friendly layout.
- **Icons for Clarity**: Clear icons for user and chatbot interactions enhance readability and user engagement.

## Demo

![Demo GIF](demo.gif)

## Installation

### Prerequisites

- Python 3.6+
- Flask
- Scikit-learn
- NLTK
- Pandas
- Pickle

### Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/mindcare-chatbot.git
    cd mindcare-chatbot
    ```

2. Create a virtual environment and activate it:

    ```bash
    pipenv shell
    ```

3. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Download NLTK data:

    ```python
    import nltk
    nltk.download('wordnet')
    nltk.download('punkt')
    nltk.download('stopwords')
    ```

5. Place your model, vectorizer, and label encoder files in the `model/` directory:

    ```bash
    mkdir model
    # Copy your model.pkl, vectorizer.pkl, and label_encoder.pkl files to the model directory
    ```

## Usage

1. Run the Flask application:

    ```bash
    python app.py
    ```

2. Open your web browser and go to `http://127.0.0.1:5000/` to interact with the chatbot.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the CodeAlpha initiative for the opportunity to work on this project.
- Special thanks to everyone who supported and guided me throughout this journey.

## Contact

For any questions or feedback, feel free to reach out at fourat.gazzeh@gmail.com.