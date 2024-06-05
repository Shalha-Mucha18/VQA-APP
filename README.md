# Visual Question Answering App

![Visual Question Answering](path_to_your_image)

This project explores the ViLT (Vision-and-Language Transformer) model from Hugging Face to create a Visual Question Answering App that answers questions about images. We implement the ViLT model in two different ways: as an API using FastAPI and as an interactive app using Streamlit.

## Features

- **ViLT Model**: Utilizes the Vision-and-Language Transformer model for image and text processing.
- **FastAPI**: Provides a robust API to receive image and text inputs and return predicted answers.
- **Streamlit**: Offers a user-friendly interface with an image uploader and text input field, allowing users to interactively ask questions about images.

## Implementation Details

### FastAPI

The FastAPI implementation allows us to build a robust backend API. It receives image and text inputs and returns the predicted answer.

- **Endpoint**: `/predict`
- **Methods**: `POST`
- **Inputs**: 
  - `image`: An image file
  - `question`: A text string
- **Output**: 
  - `answer`: The predicted answer to the question about the image

### Streamlit

The Streamlit implementation provides a user-friendly frontend interface where users can upload an image and enter a question. The app then displays the predicted answer.

- **Features**:
  - Image uploader
  - Text input field for questions
  - Display the predicted answer

## Getting Started

### Prerequisites

- Python 3.10+
- FastAPI
- Streamlit
- Hugging Face Transformers
- Pillow

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/visual-question-answering-app.git
    cd visual-question-answering-app
    ```

2. Create a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

### Running the FastAPI Server

1. Navigate to the `api` directory:
    ```bash
    cd api
    ```

2. Start the FastAPI server:
    ```bash
    uvicorn main:app --reload
    ```

3. The API will be available at `http://127.0.0.1:8000`.

### Running the Streamlit App

1. Navigate to the `streamlit_app` directory:
    ```bash
    cd streamlit_app
    ```

2. Start the Streamlit app:
    ```bash
    streamlit run app.py
    ```

3. The Streamlit interface will be available at `http://localhost:8501`.

## Usage

### FastAPI

To use the FastAPI endpoint, you can send a POST request to `http://127.0.0.1:8000/predict` with the image and question. Here's an example using `curl`:

```bash
curl -X POST "http://127.0.0.1:8000/predict" -F "image=@path_to_your_image.jpg" -F "question=Your question here"

